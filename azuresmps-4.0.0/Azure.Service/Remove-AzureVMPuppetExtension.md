---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076443"
---
# <span data-ttu-id="3bc5a-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="3bc5a-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="3bc5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc5a-103">Удаляет расширение Puppet, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="3bc5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bc5a-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3bc5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc5a-106">Командлет **Remove-AzureVMPuppetExtension** удаляет расширение Puppet, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="3bc5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc5a-108">Пример 1: удаление расширения Puppet, примененного на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="3bc5a-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="3bc5a-109">Эта команда удаляет расширение Puppet, примененное на указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="3bc5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bc5a-110">PARAMETERS</span></span>

### <span data-ttu-id="3bc5a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3bc5a-111">-InformationAction</span></span>
<span data-ttu-id="3bc5a-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3bc5a-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3bc5a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3bc5a-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3bc5a-114">Continue</span></span>
- <span data-ttu-id="3bc5a-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3bc5a-115">Ignore</span></span>
- <span data-ttu-id="3bc5a-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3bc5a-116">Inquire</span></span>
- <span data-ttu-id="3bc5a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3bc5a-117">SilentlyContinue</span></span>
- <span data-ttu-id="3bc5a-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="3bc5a-118">Stop</span></span>
- <span data-ttu-id="3bc5a-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="3bc5a-119">Suspend</span></span>

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

### <span data-ttu-id="3bc5a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3bc5a-120">-InformationVariable</span></span>
<span data-ttu-id="3bc5a-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3bc5a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="3bc5a-122">-Profile</span></span>
<span data-ttu-id="3bc5a-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3bc5a-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3bc5a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3bc5a-125">-VM</span></span>
<span data-ttu-id="3bc5a-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3bc5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc5a-127">CommonParameters</span></span>
<span data-ttu-id="3bc5a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bc5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc5a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc5a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc5a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bc5a-130">INPUTS</span></span>

## <span data-ttu-id="3bc5a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bc5a-131">OUTPUTS</span></span>

## <span data-ttu-id="3bc5a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bc5a-132">NOTES</span></span>

## <span data-ttu-id="3bc5a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bc5a-133">RELATED LINKS</span></span>

[<span data-ttu-id="3bc5a-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="3bc5a-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="3bc5a-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="3bc5a-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


