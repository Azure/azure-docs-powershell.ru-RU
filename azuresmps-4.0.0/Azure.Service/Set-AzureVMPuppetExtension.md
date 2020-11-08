---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075849"
---
# <span data-ttu-id="28d41-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="28d41-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="28d41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28d41-102">SYNOPSIS</span></span>
<span data-ttu-id="28d41-103">Задает расширение Puppet для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28d41-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="28d41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28d41-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="28d41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d41-105">DESCRIPTION</span></span>
<span data-ttu-id="28d41-106">Командлет **Set-AzureVMPuppetExtension** задает расширение Puppet для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28d41-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="28d41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28d41-107">EXAMPLES</span></span>

### <span data-ttu-id="28d41-108">Пример 1: Установка расширения Puppet для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="28d41-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="28d41-109">В этом примере задается расширение Puppet для указанной виртуальной машины в соответствии с переменной, которое хранится в $VM.</span><span class="sxs-lookup"><span data-stu-id="28d41-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="28d41-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28d41-110">PARAMETERS</span></span>

### <span data-ttu-id="28d41-111">-Отключение</span><span class="sxs-lookup"><span data-stu-id="28d41-111">-Disable</span></span>
<span data-ttu-id="28d41-112">Указывает на то, что этот командлет отключает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="28d41-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d41-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="28d41-113">-InformationAction</span></span>
<span data-ttu-id="28d41-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="28d41-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28d41-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28d41-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28d41-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="28d41-116">Continue</span></span>
- <span data-ttu-id="28d41-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="28d41-117">Ignore</span></span>
- <span data-ttu-id="28d41-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="28d41-118">Inquire</span></span>
- <span data-ttu-id="28d41-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="28d41-119">SilentlyContinue</span></span>
- <span data-ttu-id="28d41-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="28d41-120">Stop</span></span>
- <span data-ttu-id="28d41-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="28d41-121">Suspend</span></span>

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

### <span data-ttu-id="28d41-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="28d41-122">-InformationVariable</span></span>
<span data-ttu-id="28d41-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="28d41-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28d41-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="28d41-124">-Profile</span></span>
<span data-ttu-id="28d41-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="28d41-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28d41-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28d41-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28d41-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="28d41-127">-PuppetMasterServer</span></span>
<span data-ttu-id="28d41-128">Указывает полное доменное имя (FQDN) основного сервера Puppet.</span><span class="sxs-lookup"><span data-stu-id="28d41-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="28d41-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="28d41-129">-ReferenceName</span></span>
<span data-ttu-id="28d41-130">Указывает имя ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="28d41-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="28d41-131">Это определяемая пользователем строка, используемая для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="28d41-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="28d41-132">Оно указывается при первом добавлении расширения на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="28d41-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="28d41-133">При последующих обновлениях необходимо указать ранее использованный эталонный код при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="28d41-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="28d41-134">ReferenceName, назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="28d41-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d41-135">-Version</span><span class="sxs-lookup"><span data-stu-id="28d41-135">-Version</span></span>
<span data-ttu-id="28d41-136">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="28d41-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="28d41-137">-VM</span><span class="sxs-lookup"><span data-stu-id="28d41-137">-VM</span></span>
<span data-ttu-id="28d41-138">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28d41-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="28d41-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d41-139">CommonParameters</span></span>
<span data-ttu-id="28d41-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28d41-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d41-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d41-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d41-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28d41-142">INPUTS</span></span>

## <span data-ttu-id="28d41-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d41-143">OUTPUTS</span></span>

## <span data-ttu-id="28d41-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="28d41-144">NOTES</span></span>

## <span data-ttu-id="28d41-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28d41-145">RELATED LINKS</span></span>

[<span data-ttu-id="28d41-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28d41-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


