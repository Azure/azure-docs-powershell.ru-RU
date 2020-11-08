---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076354"
---
# <span data-ttu-id="a5a43-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a5a43-101">Get-AzureDisk</span></span>

## <span data-ttu-id="a5a43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5a43-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a43-103">Получение сведений о дисках в репозитории дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a43-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="a5a43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5a43-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a5a43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a43-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a43-106">Командлет **Get-AzureDisk** получает сведения о дисках, которые хранятся в репозитории дисков Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="a5a43-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="a5a43-107">Этот командлет возвращает список сведений для всех дисков в репозитории.</span><span class="sxs-lookup"><span data-stu-id="a5a43-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="a5a43-108">Чтобы просмотреть сведения о конкретном диске, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="a5a43-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="a5a43-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5a43-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a43-110">Пример 1: получение сведений о диске</span><span class="sxs-lookup"><span data-stu-id="a5a43-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="a5a43-111">Эта команда возвращает данные о диске с именем ContosoDataDisk из репозитория дисков.</span><span class="sxs-lookup"><span data-stu-id="a5a43-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="a5a43-112">Пример 2: получение сведений обо всех дисках</span><span class="sxs-lookup"><span data-stu-id="a5a43-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="a5a43-113">Эта команда получает сведения обо всех дисках в репозитории дисков.</span><span class="sxs-lookup"><span data-stu-id="a5a43-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="a5a43-114">Пример 3: получение сведений о диске</span><span class="sxs-lookup"><span data-stu-id="a5a43-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="a5a43-115">Эта команда получает данные для всех дисков в репозитории дисков, которые в настоящее время не подключены к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a5a43-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="a5a43-116">Команда получает сведения обо всех дисках и передает каждый объект в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="a5a43-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="a5a43-117">Этот командлет удаляет диск, для свойства **AttachedTo** которого не задано значение $null.</span><span class="sxs-lookup"><span data-stu-id="a5a43-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="a5a43-118">Команда форматирует список в виде таблицы с помощью командлета **Format-Table** .</span><span class="sxs-lookup"><span data-stu-id="a5a43-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="a5a43-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5a43-119">PARAMETERS</span></span>

### <span data-ttu-id="a5a43-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a5a43-120">-DiskName</span></span>
<span data-ttu-id="a5a43-121">Указывает имя диска в репозитории дисков, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="a5a43-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a43-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a5a43-122">-InformationAction</span></span>
<span data-ttu-id="a5a43-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a5a43-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a5a43-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a5a43-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5a43-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a5a43-125">Continue</span></span>
- <span data-ttu-id="a5a43-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a5a43-126">Ignore</span></span>
- <span data-ttu-id="a5a43-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a5a43-127">Inquire</span></span>
- <span data-ttu-id="a5a43-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a5a43-128">SilentlyContinue</span></span>
- <span data-ttu-id="a5a43-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="a5a43-129">Stop</span></span>
- <span data-ttu-id="a5a43-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="a5a43-130">Suspend</span></span>

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

### <span data-ttu-id="a5a43-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a5a43-131">-InformationVariable</span></span>
<span data-ttu-id="a5a43-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a5a43-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a5a43-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="a5a43-133">-Profile</span></span>
<span data-ttu-id="a5a43-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a5a43-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5a43-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5a43-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5a43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a43-136">CommonParameters</span></span>
<span data-ttu-id="a5a43-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5a43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a43-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a43-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a43-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5a43-139">INPUTS</span></span>

## <span data-ttu-id="a5a43-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a43-140">OUTPUTS</span></span>

## <span data-ttu-id="a5a43-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5a43-141">NOTES</span></span>

## <span data-ttu-id="a5a43-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5a43-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5a43-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a5a43-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="a5a43-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a5a43-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="a5a43-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a5a43-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


