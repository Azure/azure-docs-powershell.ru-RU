---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076393"
---
# <span data-ttu-id="16c01-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16c01-101">Add-AzureDisk</span></span>

## <span data-ttu-id="16c01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16c01-102">SYNOPSIS</span></span>
<span data-ttu-id="16c01-103">Добавляет диск в репозиторий диска Azure.</span><span class="sxs-lookup"><span data-stu-id="16c01-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="16c01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16c01-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c01-105">DESCRIPTION</span></span>
<span data-ttu-id="16c01-106">Командлет **Add-AzureDisk** добавляет диск в репозиторий дисков Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="16c01-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="16c01-107">Этот командлет может добавить системный диск или диск с данными.</span><span class="sxs-lookup"><span data-stu-id="16c01-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="16c01-108">Чтобы добавить системный диск, укажите тип операционной системы с помощью параметра *ОС* .</span><span class="sxs-lookup"><span data-stu-id="16c01-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="16c01-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16c01-109">EXAMPLES</span></span>

### <span data-ttu-id="16c01-110">Пример 1: Добавление загрузочного диска, использующего операционную систему Windows</span><span class="sxs-lookup"><span data-stu-id="16c01-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="16c01-111">Эта команда добавляет системный диск в репозиторий диска.</span><span class="sxs-lookup"><span data-stu-id="16c01-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="16c01-112">Системный диск использует операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="16c01-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="16c01-113">Пример 2: Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="16c01-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="16c01-114">Эта команда добавляет диск с данными.</span><span class="sxs-lookup"><span data-stu-id="16c01-114">This command adds a data disk.</span></span>

### <span data-ttu-id="16c01-115">Пример 3: Добавление системного диска Linux</span><span class="sxs-lookup"><span data-stu-id="16c01-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="16c01-116">Эта команда добавляет системный диск Linux.</span><span class="sxs-lookup"><span data-stu-id="16c01-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="16c01-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16c01-117">PARAMETERS</span></span>

### <span data-ttu-id="16c01-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="16c01-118">-DiskName</span></span>
<span data-ttu-id="16c01-119">Указывает имя диска, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="16c01-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="16c01-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="16c01-120">-InformationAction</span></span>
<span data-ttu-id="16c01-121">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="16c01-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="16c01-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="16c01-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16c01-123">Продолжал</span><span class="sxs-lookup"><span data-stu-id="16c01-123">Continue</span></span>
- <span data-ttu-id="16c01-124">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="16c01-124">Ignore</span></span>
- <span data-ttu-id="16c01-125">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="16c01-125">Inquire</span></span>
- <span data-ttu-id="16c01-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="16c01-126">SilentlyContinue</span></span>
- <span data-ttu-id="16c01-127">Остановить</span><span class="sxs-lookup"><span data-stu-id="16c01-127">Stop</span></span>
- <span data-ttu-id="16c01-128">Рвать</span><span class="sxs-lookup"><span data-stu-id="16c01-128">Suspend</span></span>

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

### <span data-ttu-id="16c01-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="16c01-129">-InformationVariable</span></span>
<span data-ttu-id="16c01-130">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="16c01-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="16c01-131">-Label</span><span class="sxs-lookup"><span data-stu-id="16c01-131">-Label</span></span>
<span data-ttu-id="16c01-132">Указывает метку диска для диска, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="16c01-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c01-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="16c01-133">-MediaLocation</span></span>
<span data-ttu-id="16c01-134">Указывает физическое расположение диска в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="16c01-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="16c01-135">Это значение ссылается на страницу большого двоичного объекта в текущей подписке и учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="16c01-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="16c01-136">-OS</span><span class="sxs-lookup"><span data-stu-id="16c01-136">-OS</span></span>
<span data-ttu-id="16c01-137">Указывает тип операционной системы для системного диска.</span><span class="sxs-lookup"><span data-stu-id="16c01-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="16c01-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="16c01-138">Valid values are:</span></span> 

- <span data-ttu-id="16c01-139">Windows</span><span class="sxs-lookup"><span data-stu-id="16c01-139">Windows</span></span> 
- <span data-ttu-id="16c01-140">Linux</span><span class="sxs-lookup"><span data-stu-id="16c01-140">Linux</span></span> 

<span data-ttu-id="16c01-141">Если этот параметр не указан, командлет добавляет диск как диск с данными.</span><span class="sxs-lookup"><span data-stu-id="16c01-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c01-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="16c01-142">-Profile</span></span>
<span data-ttu-id="16c01-143">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="16c01-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16c01-144">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16c01-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16c01-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c01-145">CommonParameters</span></span>
<span data-ttu-id="16c01-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16c01-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c01-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c01-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c01-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16c01-148">INPUTS</span></span>

## <span data-ttu-id="16c01-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c01-149">OUTPUTS</span></span>

### <span data-ttu-id="16c01-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="16c01-150">DiskContext</span></span>

## <span data-ttu-id="16c01-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="16c01-151">NOTES</span></span>

## <span data-ttu-id="16c01-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c01-152">RELATED LINKS</span></span>

[<span data-ttu-id="16c01-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16c01-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="16c01-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16c01-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="16c01-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16c01-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


