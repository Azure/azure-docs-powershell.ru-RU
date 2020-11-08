---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075501"
---
# <span data-ttu-id="c87ce-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c87ce-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="c87ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c87ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c87ce-103">Удаляет расширения ресурсов из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c87ce-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="c87ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c87ce-104">SYNTAX</span></span>

### <span data-ttu-id="c87ce-105">RemoveByExtensionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c87ce-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c87ce-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="c87ce-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c87ce-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="c87ce-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c87ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ce-108">DESCRIPTION</span></span>
<span data-ttu-id="c87ce-109">Командлет **Remove-AzureVMExtension** удаляет расширения ресурсов из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c87ce-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="c87ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c87ce-110">EXAMPLES</span></span>

### <span data-ttu-id="c87ce-111">Пример 1: удаление расширения с помощью определенного имени и издателя</span><span class="sxs-lookup"><span data-stu-id="c87ce-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="c87ce-112">Эта команда удаляет расширение с указанным именем и издателем.</span><span class="sxs-lookup"><span data-stu-id="c87ce-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="c87ce-113">Пример 2: удаление всех расширений с определенной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="c87ce-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="c87ce-114">Эта команда удаляет все расширения с указанной виртуальной машины, хранящиеся в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="c87ce-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="c87ce-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c87ce-115">PARAMETERS</span></span>

### <span data-ttu-id="c87ce-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c87ce-116">-ExtensionName</span></span>
<span data-ttu-id="c87ce-117">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c87ce-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ce-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c87ce-118">-InformationAction</span></span>
<span data-ttu-id="c87ce-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c87ce-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c87ce-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c87ce-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c87ce-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c87ce-121">Continue</span></span>
- <span data-ttu-id="c87ce-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c87ce-122">Ignore</span></span>
- <span data-ttu-id="c87ce-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c87ce-123">Inquire</span></span>
- <span data-ttu-id="c87ce-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c87ce-124">SilentlyContinue</span></span>
- <span data-ttu-id="c87ce-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="c87ce-125">Stop</span></span>
- <span data-ttu-id="c87ce-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="c87ce-126">Suspend</span></span>

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

### <span data-ttu-id="c87ce-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c87ce-127">-InformationVariable</span></span>
<span data-ttu-id="c87ce-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c87ce-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c87ce-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="c87ce-129">-Profile</span></span>
<span data-ttu-id="c87ce-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c87ce-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c87ce-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c87ce-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c87ce-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c87ce-132">-Publisher</span></span>
<span data-ttu-id="c87ce-133">Указывает издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="c87ce-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ce-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="c87ce-134">-ReferenceName</span></span>
<span data-ttu-id="c87ce-135">Указывает имя ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="c87ce-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ce-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="c87ce-136">-RemoveAll</span></span>
<span data-ttu-id="c87ce-137">Указывает на то, что этот командлет удаляет все расширения ресурсов из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c87ce-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ce-138">-VM</span><span class="sxs-lookup"><span data-stu-id="c87ce-138">-VM</span></span>
<span data-ttu-id="c87ce-139">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c87ce-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c87ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87ce-140">CommonParameters</span></span>
<span data-ttu-id="c87ce-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c87ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87ce-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87ce-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87ce-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c87ce-143">INPUTS</span></span>

## <span data-ttu-id="c87ce-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ce-144">OUTPUTS</span></span>

## <span data-ttu-id="c87ce-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="c87ce-145">NOTES</span></span>

## <span data-ttu-id="c87ce-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c87ce-146">RELATED LINKS</span></span>

[<span data-ttu-id="c87ce-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c87ce-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="c87ce-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c87ce-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


