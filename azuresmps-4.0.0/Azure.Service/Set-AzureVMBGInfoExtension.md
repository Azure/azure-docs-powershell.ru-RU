---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076043"
---
# <span data-ttu-id="d05e5-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="d05e5-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="d05e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d05e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d05e5-103">Задает расширение BGInfo для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d05e5-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="d05e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d05e5-104">SYNTAX</span></span>

### <span data-ttu-id="d05e5-105">SetBGInfoExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d05e5-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d05e5-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="d05e5-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d05e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d05e5-107">DESCRIPTION</span></span>
<span data-ttu-id="d05e5-108">Командлет **Set-AzureVMBGInfoExtension** задает расширение BGInfo для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d05e5-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="d05e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d05e5-109">EXAMPLES</span></span>

### <span data-ttu-id="d05e5-110">Пример 1: Установка расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d05e5-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="d05e5-111">Эта команда задает расширение BGInfo для указанной виртуальной машины, сохраненное в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="d05e5-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="d05e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d05e5-112">PARAMETERS</span></span>

### <span data-ttu-id="d05e5-113">-Отключение</span><span class="sxs-lookup"><span data-stu-id="d05e5-113">-Disable</span></span>
<span data-ttu-id="d05e5-114">Указывает на то, что этот командлет отключает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="d05e5-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e5-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d05e5-115">-InformationAction</span></span>
<span data-ttu-id="d05e5-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d05e5-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d05e5-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d05e5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d05e5-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d05e5-118">Continue</span></span>
- <span data-ttu-id="d05e5-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d05e5-119">Ignore</span></span>
- <span data-ttu-id="d05e5-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d05e5-120">Inquire</span></span>
- <span data-ttu-id="d05e5-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d05e5-121">SilentlyContinue</span></span>
- <span data-ttu-id="d05e5-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="d05e5-122">Stop</span></span>
- <span data-ttu-id="d05e5-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="d05e5-123">Suspend</span></span>

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

### <span data-ttu-id="d05e5-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d05e5-124">-InformationVariable</span></span>
<span data-ttu-id="d05e5-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d05e5-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d05e5-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="d05e5-126">-Profile</span></span>
<span data-ttu-id="d05e5-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d05e5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d05e5-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d05e5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d05e5-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="d05e5-129">-ReferenceName</span></span>
<span data-ttu-id="d05e5-130">Указывает имя ссылки расширения BGInfo.</span><span class="sxs-lookup"><span data-stu-id="d05e5-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="d05e5-131">Этот параметр является пользовательской строкой, которую можно использовать для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="d05e5-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="d05e5-132">Оно указывается при первом добавлении расширения на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d05e5-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="d05e5-133">Вы можете указать ранее использованное имя ссылки при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="d05e5-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e5-134">-Удаление</span><span class="sxs-lookup"><span data-stu-id="d05e5-134">-Uninstall</span></span>
<span data-ttu-id="d05e5-135">Указывает на то, что этот командлет удаляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="d05e5-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e5-136">-Version</span><span class="sxs-lookup"><span data-stu-id="d05e5-136">-Version</span></span>
<span data-ttu-id="d05e5-137">Указывает версию расширения BGInfo.</span><span class="sxs-lookup"><span data-stu-id="d05e5-137">Specifies the version of the BGInfo extension.</span></span>

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

### <span data-ttu-id="d05e5-138">-VM</span><span class="sxs-lookup"><span data-stu-id="d05e5-138">-VM</span></span>
<span data-ttu-id="d05e5-139">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d05e5-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d05e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05e5-140">CommonParameters</span></span>
<span data-ttu-id="d05e5-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d05e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05e5-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05e5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05e5-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d05e5-143">INPUTS</span></span>

## <span data-ttu-id="d05e5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d05e5-144">OUTPUTS</span></span>

## <span data-ttu-id="d05e5-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d05e5-145">NOTES</span></span>

## <span data-ttu-id="d05e5-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d05e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="d05e5-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="d05e5-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="d05e5-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="d05e5-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


