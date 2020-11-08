---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075425"
---
# <span data-ttu-id="b62af-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b62af-101">Update-AzureDisk</span></span>

## <span data-ttu-id="b62af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b62af-102">SYNOPSIS</span></span>
<span data-ttu-id="b62af-103">Изменяет метку диска в репозитории дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="b62af-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="b62af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b62af-104">SYNTAX</span></span>

### <span data-ttu-id="b62af-105">Изменение размера</span><span class="sxs-lookup"><span data-stu-id="b62af-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b62af-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="b62af-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b62af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62af-107">DESCRIPTION</span></span>
<span data-ttu-id="b62af-108">Командлет **Update-AzureDisk** изменяет метку, связанную с диском в репозитории текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="b62af-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="b62af-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b62af-109">EXAMPLES</span></span>

### <span data-ttu-id="b62af-110">Пример 1: изменение метки диска</span><span class="sxs-lookup"><span data-stu-id="b62af-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="b62af-111">Эта команда изменяет метку диска с именем ContosoOSDisk на DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="b62af-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="b62af-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b62af-112">PARAMETERS</span></span>

### <span data-ttu-id="b62af-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b62af-113">-DiskName</span></span>
<span data-ttu-id="b62af-114">Указывает имя диска, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b62af-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62af-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b62af-115">-InformationAction</span></span>
<span data-ttu-id="b62af-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b62af-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b62af-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b62af-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b62af-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b62af-118">Continue</span></span>
- <span data-ttu-id="b62af-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b62af-119">Ignore</span></span>
- <span data-ttu-id="b62af-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b62af-120">Inquire</span></span>
- <span data-ttu-id="b62af-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b62af-121">SilentlyContinue</span></span>
- <span data-ttu-id="b62af-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="b62af-122">Stop</span></span>
- <span data-ttu-id="b62af-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="b62af-123">Suspend</span></span>

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

### <span data-ttu-id="b62af-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b62af-124">-InformationVariable</span></span>
<span data-ttu-id="b62af-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b62af-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b62af-126">-Label</span><span class="sxs-lookup"><span data-stu-id="b62af-126">-Label</span></span>
<span data-ttu-id="b62af-127">Задает новую метку для диска.</span><span class="sxs-lookup"><span data-stu-id="b62af-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62af-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="b62af-128">-Profile</span></span>
<span data-ttu-id="b62af-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b62af-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b62af-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b62af-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b62af-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b62af-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="b62af-132">Указывает новый размер диска (в гигабайтах).</span><span class="sxs-lookup"><span data-stu-id="b62af-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62af-133">CommonParameters</span></span>
<span data-ttu-id="b62af-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b62af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62af-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62af-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62af-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b62af-136">INPUTS</span></span>

## <span data-ttu-id="b62af-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62af-137">OUTPUTS</span></span>

### <span data-ttu-id="b62af-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="b62af-138">DiskContext</span></span>

## <span data-ttu-id="b62af-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b62af-139">NOTES</span></span>

## <span data-ttu-id="b62af-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b62af-140">RELATED LINKS</span></span>

[<span data-ttu-id="b62af-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b62af-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="b62af-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b62af-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="b62af-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b62af-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


