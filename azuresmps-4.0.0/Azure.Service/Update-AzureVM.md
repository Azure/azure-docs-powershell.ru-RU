---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076013"
---
# <span data-ttu-id="1e665-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-101">Update-AzureVM</span></span>

## <span data-ttu-id="1e665-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e665-102">SYNOPSIS</span></span>
<span data-ttu-id="1e665-103">Изменение конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="1e665-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="1e665-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e665-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e665-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e665-105">DESCRIPTION</span></span>
<span data-ttu-id="1e665-106">Командлет **Update-AzureVM** принимает сведения об обновлении для указанной виртуальной машины и инициирует обновление.</span><span class="sxs-lookup"><span data-stu-id="1e665-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="1e665-107">Вы можете добавлять и удалять диски с данными, изменять режим кэширования дисков данных или операционной системы, изменять конечные точки сети или изменять размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1e665-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="1e665-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e665-108">EXAMPLES</span></span>

### <span data-ttu-id="1e665-109">Пример 1: Обновление размера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1e665-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="1e665-110">Эта команда изменяет размер виртуальной машины с именем VirtualMachine04, работающей в службе с именем ContosoService03, в значение Medium.</span><span class="sxs-lookup"><span data-stu-id="1e665-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="1e665-111">Пример 2: Добавление диска с данными на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="1e665-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="1e665-112">Эта команда добавляет новый диск с данными на виртуальную машину с именем VirtualMachine05 и выполняется в службе с именем ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="1e665-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="1e665-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e665-113">PARAMETERS</span></span>

### <span data-ttu-id="1e665-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e665-114">-InformationAction</span></span>
<span data-ttu-id="1e665-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="1e665-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e665-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1e665-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e665-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="1e665-117">Continue</span></span>
- <span data-ttu-id="1e665-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="1e665-118">Ignore</span></span>
- <span data-ttu-id="1e665-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="1e665-119">Inquire</span></span>
- <span data-ttu-id="1e665-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e665-120">SilentlyContinue</span></span>
- <span data-ttu-id="1e665-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="1e665-121">Stop</span></span>
- <span data-ttu-id="1e665-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="1e665-122">Suspend</span></span>

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

### <span data-ttu-id="1e665-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e665-123">-InformationVariable</span></span>
<span data-ttu-id="1e665-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="1e665-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e665-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e665-125">-Name</span></span>
<span data-ttu-id="1e665-126">Указывает имя обновляемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1e665-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="1e665-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="1e665-127">-Profile</span></span>
<span data-ttu-id="1e665-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1e665-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e665-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e665-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e665-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1e665-130">-ServiceName</span></span>
<span data-ttu-id="1e665-131">Указывает имя службы Azure.</span><span class="sxs-lookup"><span data-stu-id="1e665-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="1e665-132">-VM</span><span class="sxs-lookup"><span data-stu-id="1e665-132">-VM</span></span>
<span data-ttu-id="1e665-133">Указывает объект виртуальной машины, включающий обновленные параметры.</span><span class="sxs-lookup"><span data-stu-id="1e665-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e665-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e665-134">CommonParameters</span></span>
<span data-ttu-id="1e665-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e665-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e665-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e665-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e665-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e665-137">INPUTS</span></span>

## <span data-ttu-id="1e665-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e665-138">OUTPUTS</span></span>

## <span data-ttu-id="1e665-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e665-139">NOTES</span></span>

## <span data-ttu-id="1e665-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e665-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e665-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1e665-142">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="1e665-143">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="1e665-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="1e665-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="1e665-145">Restarts-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="1e665-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="1e665-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="1e665-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="1e665-148">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1e665-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


