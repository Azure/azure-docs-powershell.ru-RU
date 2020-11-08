---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075811"
---
# <span data-ttu-id="2b4a4-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2b4a4-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="2b4a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4a4-103">Задает расширение VMAccess для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="2b4a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b4a4-104">SYNTAX</span></span>

### <span data-ttu-id="2b4a4-105">EnableAccessExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b4a4-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b4a4-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2b4a4-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b4a4-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2b4a4-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2b4a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b4a4-108">DESCRIPTION</span></span>
<span data-ttu-id="2b4a4-109">Командлет **Set-AzureVMAccessExtension** добавляет расширение виртуальной машины VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="2b4a4-110">Вы можете использовать расширение VMAccess, чтобы установить временный пароль, и его следует немедленно изменить после входа на компьютер.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="2b4a4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b4a4-111">EXAMPLES</span></span>

### <span data-ttu-id="2b4a4-112">Пример 1: Установка расширения VMAccess, примененного к указанной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="2b4a4-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="2b4a4-113">Эта команда задает расширение VMAccess, применяемое к указанной виртуальной машине, в соответствии с переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="2b4a4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b4a4-114">PARAMETERS</span></span>

### <span data-ttu-id="2b4a4-115">-Отключение</span><span class="sxs-lookup"><span data-stu-id="2b4a4-115">-Disable</span></span>
<span data-ttu-id="2b4a4-116">Указывает, что этот командлет задает состояние расширения для отключения.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2b4a4-117">-ForceUpdate</span></span>
<span data-ttu-id="2b4a4-118">Указывает на то, что этот командлет снова применяет конфигурацию к расширению, когда конфигурация не была обновлена.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2b4a4-119">-InformationAction</span></span>
<span data-ttu-id="2b4a4-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2b4a4-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2b4a4-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b4a4-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2b4a4-122">Continue</span></span>
- <span data-ttu-id="2b4a4-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2b4a4-123">Ignore</span></span>
- <span data-ttu-id="2b4a4-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2b4a4-124">Inquire</span></span>
- <span data-ttu-id="2b4a4-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2b4a4-125">SilentlyContinue</span></span>
- <span data-ttu-id="2b4a4-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="2b4a4-126">Stop</span></span>
- <span data-ttu-id="2b4a4-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="2b4a4-127">Suspend</span></span>

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

### <span data-ttu-id="2b4a4-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2b4a4-128">-InformationVariable</span></span>
<span data-ttu-id="2b4a4-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2b4a4-130">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="2b4a4-130">-Password</span></span>
<span data-ttu-id="2b4a4-131">Указывает пароль для сброса учетных данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b4a4-132">-Profile</span></span>
<span data-ttu-id="2b4a4-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b4a4-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b4a4-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="2b4a4-135">-ReferenceName</span></span>
<span data-ttu-id="2b4a4-136">Указывает имя ссылки на расширение Access.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="2b4a4-137">Это определяемая пользователем строка, используемая для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="2b4a4-138">Оно указывается при первом добавлении расширения на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="2b4a4-139">При последующих обновлениях необходимо указать ранее использованное имя ссылки при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="2b4a4-140">*ReferenceName* , назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2b4a4-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-141">-Удаление</span><span class="sxs-lookup"><span data-stu-id="2b4a4-141">-Uninstall</span></span>
<span data-ttu-id="2b4a4-142">Указывает, удаляет ли этот командлет расширение Access.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="2b4a4-143">-UserName</span></span>
<span data-ttu-id="2b4a4-144">Указывает имя пользователя, используемое этим командлетом для сброса учетных данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a4-145">-Version</span><span class="sxs-lookup"><span data-stu-id="2b4a4-145">-Version</span></span>
<span data-ttu-id="2b4a4-146">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-146">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="2b4a4-147">-VM</span><span class="sxs-lookup"><span data-stu-id="2b4a4-147">-VM</span></span>
<span data-ttu-id="2b4a4-148">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2b4a4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4a4-149">CommonParameters</span></span>
<span data-ttu-id="2b4a4-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4a4-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b4a4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4a4-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b4a4-152">INPUTS</span></span>

## <span data-ttu-id="2b4a4-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b4a4-153">OUTPUTS</span></span>

## <span data-ttu-id="2b4a4-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b4a4-154">NOTES</span></span>

## <span data-ttu-id="2b4a4-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b4a4-155">RELATED LINKS</span></span>

[<span data-ttu-id="2b4a4-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2b4a4-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="2b4a4-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2b4a4-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


