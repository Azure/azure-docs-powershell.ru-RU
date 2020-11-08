---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075505"
---
# <span data-ttu-id="bc8e6-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bc8e6-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="bc8e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8e6-103">Удаляет расширение Chef, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="bc8e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc8e6-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc8e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8e6-106">Командлет **Remove-AzureVMChefExtension** удаляет расширение Chef, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="bc8e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc8e6-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8e6-108">Пример 1: удаление расширения Chef, примененного на указанной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bc8e6-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="bc8e6-109">Эта команда удаляет расширение Chef, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="bc8e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc8e6-110">PARAMETERS</span></span>

### <span data-ttu-id="bc8e6-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bc8e6-111">-InformationAction</span></span>
<span data-ttu-id="bc8e6-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bc8e6-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc8e6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc8e6-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="bc8e6-114">Continue</span></span>
- <span data-ttu-id="bc8e6-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="bc8e6-115">Ignore</span></span>
- <span data-ttu-id="bc8e6-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="bc8e6-116">Inquire</span></span>
- <span data-ttu-id="bc8e6-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc8e6-117">SilentlyContinue</span></span>
- <span data-ttu-id="bc8e6-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="bc8e6-118">Stop</span></span>
- <span data-ttu-id="bc8e6-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="bc8e6-119">Suspend</span></span>

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

### <span data-ttu-id="bc8e6-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc8e6-120">-InformationVariable</span></span>
<span data-ttu-id="bc8e6-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc8e6-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc8e6-122">-Profile</span></span>
<span data-ttu-id="bc8e6-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc8e6-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc8e6-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bc8e6-125">-VM</span></span>
<span data-ttu-id="bc8e6-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bc8e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8e6-127">CommonParameters</span></span>
<span data-ttu-id="bc8e6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc8e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8e6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc8e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8e6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc8e6-130">INPUTS</span></span>

## <span data-ttu-id="bc8e6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc8e6-131">OUTPUTS</span></span>

## <span data-ttu-id="bc8e6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc8e6-132">NOTES</span></span>

## <span data-ttu-id="bc8e6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc8e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc8e6-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bc8e6-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="bc8e6-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bc8e6-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


