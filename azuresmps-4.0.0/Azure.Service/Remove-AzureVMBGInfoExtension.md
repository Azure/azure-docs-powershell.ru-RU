---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075508"
---
# <span data-ttu-id="627b4-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="627b4-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="627b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="627b4-102">SYNOPSIS</span></span>
<span data-ttu-id="627b4-103">Удаление расширения BGInfo, примененного к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="627b4-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="627b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="627b4-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="627b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="627b4-105">DESCRIPTION</span></span>
<span data-ttu-id="627b4-106">Командлет **Remove-AzureVMBGInfoExtension** удаляет расширение BGInfo, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="627b4-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="627b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="627b4-107">EXAMPLES</span></span>

### <span data-ttu-id="627b4-108">Пример 1: удаление расширения BGInfo на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="627b4-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="627b4-109">Эта команда удаляет расширение BGInfo, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="627b4-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="627b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="627b4-110">PARAMETERS</span></span>

### <span data-ttu-id="627b4-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="627b4-111">-InformationAction</span></span>
<span data-ttu-id="627b4-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="627b4-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="627b4-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="627b4-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="627b4-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="627b4-114">Continue</span></span>
- <span data-ttu-id="627b4-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="627b4-115">Ignore</span></span>
- <span data-ttu-id="627b4-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="627b4-116">Inquire</span></span>
- <span data-ttu-id="627b4-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="627b4-117">SilentlyContinue</span></span>
- <span data-ttu-id="627b4-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="627b4-118">Stop</span></span>
- <span data-ttu-id="627b4-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="627b4-119">Suspend</span></span>

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

### <span data-ttu-id="627b4-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="627b4-120">-InformationVariable</span></span>
<span data-ttu-id="627b4-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="627b4-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="627b4-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="627b4-122">-Profile</span></span>
<span data-ttu-id="627b4-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="627b4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="627b4-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="627b4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="627b4-125">-VM</span><span class="sxs-lookup"><span data-stu-id="627b4-125">-VM</span></span>
<span data-ttu-id="627b4-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="627b4-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="627b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b4-127">CommonParameters</span></span>
<span data-ttu-id="627b4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="627b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="627b4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="627b4-130">INPUTS</span></span>

## <span data-ttu-id="627b4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="627b4-131">OUTPUTS</span></span>

## <span data-ttu-id="627b4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="627b4-132">NOTES</span></span>

## <span data-ttu-id="627b4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="627b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="627b4-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="627b4-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="627b4-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="627b4-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


