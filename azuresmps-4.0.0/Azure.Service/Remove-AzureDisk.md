---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076157"
---
# <span data-ttu-id="4897e-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="4897e-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="4897e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4897e-102">SYNOPSIS</span></span>
<span data-ttu-id="4897e-103">Удаление диска из хранилища дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="4897e-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="4897e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4897e-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4897e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4897e-105">DESCRIPTION</span></span>
<span data-ttu-id="4897e-106">Командлет **Remove-AzureDisk** удаляет диск из хранилища дисков Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="4897e-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="4897e-107">По умолчанию этот командлет не удаляет файл виртуального жесткого диска (VHD) из хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="4897e-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="4897e-108">Чтобы удалить VHD, укажите параметр *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="4897e-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="4897e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4897e-109">EXAMPLES</span></span>

### <span data-ttu-id="4897e-110">Пример 1: удаление диска</span><span class="sxs-lookup"><span data-stu-id="4897e-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="4897e-111">Эта команда удаляет диск с именем ContosoDataDisk из хранилища дисков.</span><span class="sxs-lookup"><span data-stu-id="4897e-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="4897e-112">Команда не удаляет VHD.</span><span class="sxs-lookup"><span data-stu-id="4897e-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="4897e-113">Пример 2: удаление и удаление диска</span><span class="sxs-lookup"><span data-stu-id="4897e-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="4897e-114">Эта команда удаляет диск с именем ContosoDataDisk из хранилища дисков.</span><span class="sxs-lookup"><span data-stu-id="4897e-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="4897e-115">Эта команда задает параметр DeleteVHD.</span><span class="sxs-lookup"><span data-stu-id="4897e-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="4897e-116">Таким образом, команда удаляет VHD из хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4897e-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="4897e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4897e-117">PARAMETERS</span></span>

### <span data-ttu-id="4897e-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="4897e-118">-DeleteVHD</span></span>
<span data-ttu-id="4897e-119">Указывает, что этот командлет удаляет виртуальный жесткий диск из хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="4897e-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4897e-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="4897e-120">-DiskName</span></span>
<span data-ttu-id="4897e-121">Указывает имя диска данных в репозитории дисков, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4897e-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4897e-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4897e-122">-InformationAction</span></span>
<span data-ttu-id="4897e-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4897e-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4897e-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4897e-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4897e-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4897e-125">Continue</span></span>
- <span data-ttu-id="4897e-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4897e-126">Ignore</span></span>
- <span data-ttu-id="4897e-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4897e-127">Inquire</span></span>
- <span data-ttu-id="4897e-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4897e-128">SilentlyContinue</span></span>
- <span data-ttu-id="4897e-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="4897e-129">Stop</span></span>
- <span data-ttu-id="4897e-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="4897e-130">Suspend</span></span>

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

### <span data-ttu-id="4897e-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4897e-131">-InformationVariable</span></span>
<span data-ttu-id="4897e-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4897e-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4897e-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="4897e-133">-Profile</span></span>
<span data-ttu-id="4897e-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4897e-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4897e-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4897e-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4897e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4897e-136">CommonParameters</span></span>
<span data-ttu-id="4897e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4897e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4897e-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4897e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4897e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4897e-139">INPUTS</span></span>

## <span data-ttu-id="4897e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4897e-140">OUTPUTS</span></span>

## <span data-ttu-id="4897e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4897e-141">NOTES</span></span>

## <span data-ttu-id="4897e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4897e-142">RELATED LINKS</span></span>

[<span data-ttu-id="4897e-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="4897e-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="4897e-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="4897e-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="4897e-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="4897e-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


