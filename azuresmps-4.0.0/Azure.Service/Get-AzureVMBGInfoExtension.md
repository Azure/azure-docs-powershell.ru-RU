---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075532"
---
# <span data-ttu-id="f33aa-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f33aa-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="f33aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f33aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f33aa-103">Получает расширение BGInfo, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f33aa-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="f33aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f33aa-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f33aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f33aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f33aa-106">Командлет **Get-AzureVMBGInfoExtension** получает расширение BGInfo, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f33aa-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="f33aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f33aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f33aa-108">Пример 1: получение расширения BGInfo, примененного к указанной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="f33aa-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="f33aa-109">Эта команда получает расширение BGInfo, примененное к указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f33aa-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="f33aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f33aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f33aa-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f33aa-111">-InformationAction</span></span>
<span data-ttu-id="f33aa-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f33aa-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f33aa-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f33aa-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f33aa-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f33aa-114">Continue</span></span>
- <span data-ttu-id="f33aa-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f33aa-115">Ignore</span></span>
- <span data-ttu-id="f33aa-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f33aa-116">Inquire</span></span>
- <span data-ttu-id="f33aa-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f33aa-117">SilentlyContinue</span></span>
- <span data-ttu-id="f33aa-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="f33aa-118">Stop</span></span>
- <span data-ttu-id="f33aa-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="f33aa-119">Suspend</span></span>

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

### <span data-ttu-id="f33aa-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f33aa-120">-InformationVariable</span></span>
<span data-ttu-id="f33aa-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f33aa-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f33aa-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="f33aa-122">-Profile</span></span>
<span data-ttu-id="f33aa-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f33aa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f33aa-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f33aa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f33aa-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f33aa-125">-VM</span></span>
<span data-ttu-id="f33aa-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f33aa-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f33aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33aa-127">CommonParameters</span></span>
<span data-ttu-id="f33aa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f33aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33aa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33aa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f33aa-130">INPUTS</span></span>

## <span data-ttu-id="f33aa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f33aa-131">OUTPUTS</span></span>

## <span data-ttu-id="f33aa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f33aa-132">NOTES</span></span>

## <span data-ttu-id="f33aa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f33aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="f33aa-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f33aa-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="f33aa-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f33aa-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


