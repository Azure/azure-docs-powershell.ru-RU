---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076332"
---
# <span data-ttu-id="1d992-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="1d992-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="1d992-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d992-102">SYNOPSIS</span></span>
<span data-ttu-id="1d992-103">Получает диск операционной системы виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="1d992-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="1d992-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d992-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d992-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d992-105">DESCRIPTION</span></span>
<span data-ttu-id="1d992-106">Командлет **Get-AzureOSDisk** получает диск операционной системы виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="1d992-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="1d992-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d992-107">EXAMPLES</span></span>

### <span data-ttu-id="1d992-108">Пример 1: получение диска операционной системы</span><span class="sxs-lookup"><span data-stu-id="1d992-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="1d992-109">Эта команда получает виртуальную машину с именем VirtualMachine02 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1d992-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="1d992-110">Команда передает виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="1d992-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d992-111">Текущий командлет получает диск операционной системы этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d992-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="1d992-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d992-112">PARAMETERS</span></span>

### <span data-ttu-id="1d992-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1d992-113">-InformationAction</span></span>
<span data-ttu-id="1d992-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="1d992-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1d992-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1d992-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d992-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="1d992-116">Continue</span></span>
- <span data-ttu-id="1d992-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="1d992-117">Ignore</span></span>
- <span data-ttu-id="1d992-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="1d992-118">Inquire</span></span>
- <span data-ttu-id="1d992-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1d992-119">SilentlyContinue</span></span>
- <span data-ttu-id="1d992-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="1d992-120">Stop</span></span>
- <span data-ttu-id="1d992-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="1d992-121">Suspend</span></span>

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

### <span data-ttu-id="1d992-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1d992-122">-InformationVariable</span></span>
<span data-ttu-id="1d992-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="1d992-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1d992-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="1d992-124">-Profile</span></span>
<span data-ttu-id="1d992-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1d992-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d992-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d992-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d992-127">-VM</span><span class="sxs-lookup"><span data-stu-id="1d992-127">-VM</span></span>
<span data-ttu-id="1d992-128">Указывает виртуальную машину, для которой этот командлет получает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1d992-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="1d992-129">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1d992-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="1d992-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d992-130">CommonParameters</span></span>
<span data-ttu-id="1d992-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d992-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d992-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d992-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d992-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d992-133">INPUTS</span></span>

## <span data-ttu-id="1d992-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d992-134">OUTPUTS</span></span>

## <span data-ttu-id="1d992-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d992-135">NOTES</span></span>

## <span data-ttu-id="1d992-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d992-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d992-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="1d992-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="1d992-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="1d992-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


