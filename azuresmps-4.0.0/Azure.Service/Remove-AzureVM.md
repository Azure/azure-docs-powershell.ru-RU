---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075516"
---
# <span data-ttu-id="be103-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-101">Remove-AzureVM</span></span>

## <span data-ttu-id="be103-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be103-102">SYNOPSIS</span></span>
<span data-ttu-id="be103-103">Удаление виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="be103-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="be103-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be103-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be103-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be103-105">DESCRIPTION</span></span>
<span data-ttu-id="be103-106">Командлет **Remove-AzureVM** удаляет виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="be103-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="be103-107">В ходе этого процесса не удаляются базовые VHD-файлы на дисках, подключенных к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="be103-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="be103-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be103-108">EXAMPLES</span></span>

### <span data-ttu-id="be103-109">Пример 1: Удаление виртуальной машины из службы</span><span class="sxs-lookup"><span data-stu-id="be103-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="be103-110">Эта команда удаляет виртуальную машину с именем VirtualMachine03, которая запускается в службе ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="be103-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="be103-111">Пример 2: Удаление виртуальной машины и удаление VHD-файлов</span><span class="sxs-lookup"><span data-stu-id="be103-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="be103-112">Эта команда удаляет виртуальную машину VirtualMachine04, которая запускается в службе ContosoService03, и определяет удаление VHD-файлов с помощью параметра *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="be103-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="be103-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be103-113">PARAMETERS</span></span>

### <span data-ttu-id="be103-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="be103-114">-DeleteVHD</span></span>
<span data-ttu-id="be103-115">Указывает, будет ли этот командлет удалять виртуальную машину и базовые объекты BLOB-дисков.</span><span class="sxs-lookup"><span data-stu-id="be103-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be103-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="be103-116">-InformationAction</span></span>
<span data-ttu-id="be103-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="be103-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="be103-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="be103-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be103-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="be103-119">Continue</span></span>
- <span data-ttu-id="be103-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="be103-120">Ignore</span></span>
- <span data-ttu-id="be103-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="be103-121">Inquire</span></span>
- <span data-ttu-id="be103-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="be103-122">SilentlyContinue</span></span>
- <span data-ttu-id="be103-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="be103-123">Stop</span></span>
- <span data-ttu-id="be103-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="be103-124">Suspend</span></span>

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

### <span data-ttu-id="be103-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be103-125">-InformationVariable</span></span>
<span data-ttu-id="be103-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="be103-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="be103-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be103-127">-Name</span></span>
<span data-ttu-id="be103-128">Указывает имя удаляемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be103-128">Specifies the name of the virtual machine being removed.</span></span>

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

### <span data-ttu-id="be103-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="be103-129">-Profile</span></span>
<span data-ttu-id="be103-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="be103-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be103-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be103-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be103-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="be103-132">-ServiceName</span></span>
<span data-ttu-id="be103-133">Указывает имя службы Azure, из которой удаляется виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="be103-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="be103-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be103-134">-Confirm</span></span>
<span data-ttu-id="be103-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be103-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be103-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be103-136">-WhatIf</span></span>
<span data-ttu-id="be103-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be103-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be103-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be103-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be103-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be103-139">CommonParameters</span></span>
<span data-ttu-id="be103-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be103-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be103-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be103-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be103-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be103-142">INPUTS</span></span>

## <span data-ttu-id="be103-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be103-143">OUTPUTS</span></span>

## <span data-ttu-id="be103-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="be103-144">NOTES</span></span>

## <span data-ttu-id="be103-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be103-145">RELATED LINKS</span></span>

[<span data-ttu-id="be103-146">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="be103-147">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="be103-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="be103-148">Restarts-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="be103-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="be103-150">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="be103-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be103-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


