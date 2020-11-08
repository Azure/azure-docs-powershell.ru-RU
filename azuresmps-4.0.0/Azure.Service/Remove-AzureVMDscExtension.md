---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076447"
---
# <span data-ttu-id="aca63-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aca63-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="aca63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aca63-102">SYNOPSIS</span></span>
<span data-ttu-id="aca63-103">Удаляет расширение DSC Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca63-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="aca63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aca63-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aca63-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca63-105">DESCRIPTION</span></span>
<span data-ttu-id="aca63-106">Командлет **Remove-AzureVMDscExtension** УДАЛЯЕТ расширение DSC Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca63-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="aca63-107">Выходные данные этого командлета должны передаваться командлету **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="aca63-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="aca63-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aca63-108">EXAMPLES</span></span>

### <span data-ttu-id="aca63-109">Пример 1: удаление расширения DSC из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="aca63-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="aca63-110">Эта команда удаляет расширение DSC Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca63-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="aca63-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aca63-111">PARAMETERS</span></span>

### <span data-ttu-id="aca63-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aca63-112">-InformationAction</span></span>
<span data-ttu-id="aca63-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="aca63-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aca63-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aca63-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aca63-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="aca63-115">Continue</span></span>
- <span data-ttu-id="aca63-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="aca63-116">Ignore</span></span>
- <span data-ttu-id="aca63-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="aca63-117">Inquire</span></span>
- <span data-ttu-id="aca63-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aca63-118">SilentlyContinue</span></span>
- <span data-ttu-id="aca63-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="aca63-119">Stop</span></span>
- <span data-ttu-id="aca63-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="aca63-120">Suspend</span></span>

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

### <span data-ttu-id="aca63-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aca63-121">-InformationVariable</span></span>
<span data-ttu-id="aca63-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="aca63-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aca63-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="aca63-123">-Profile</span></span>
<span data-ttu-id="aca63-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aca63-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aca63-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aca63-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aca63-126">-VM</span><span class="sxs-lookup"><span data-stu-id="aca63-126">-VM</span></span>
<span data-ttu-id="aca63-127">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca63-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="aca63-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aca63-128">-Confirm</span></span>
<span data-ttu-id="aca63-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aca63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca63-130">-WhatIf</span></span>
<span data-ttu-id="aca63-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aca63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca63-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aca63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aca63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca63-133">CommonParameters</span></span>
<span data-ttu-id="aca63-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aca63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca63-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca63-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca63-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aca63-136">INPUTS</span></span>

## <span data-ttu-id="aca63-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca63-137">OUTPUTS</span></span>

## <span data-ttu-id="aca63-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aca63-138">NOTES</span></span>

## <span data-ttu-id="aca63-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aca63-139">RELATED LINKS</span></span>

[<span data-ttu-id="aca63-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aca63-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="aca63-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aca63-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="aca63-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aca63-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


