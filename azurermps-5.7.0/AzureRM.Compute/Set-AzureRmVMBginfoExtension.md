---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559156"
---
# <span data-ttu-id="d6887-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d6887-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="d6887-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6887-102">SYNOPSIS</span></span>
<span data-ttu-id="d6887-103">Добавляет расширение BGInfo к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d6887-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6887-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6887-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6887-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6887-105">DESCRIPTION</span></span>
<span data-ttu-id="d6887-106">Командлет **Set-AzureRmVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d6887-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="d6887-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6887-107">EXAMPLES</span></span>

### <span data-ttu-id="d6887-108">Пример 1: Добавление расширения BGInfo на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="d6887-108">Example 1: Add the BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
<span data-ttu-id="d6887-109">Эта команда добавляет расширение BGInfo на виртуальную машину с именем ContosoVM в группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="d6887-109">This command adds the BGInfo extension to a virtual machine named ContosoVM in the resource group ContosoRG.</span></span>

### <span data-ttu-id="d6887-110">Пример 2: Добавление определенной версии расширения BGInfo на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="d6887-110">Example 2: Add a specific version of BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="d6887-111">Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="d6887-111">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="d6887-112">Команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6887-112">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="d6887-113">Команда задает имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="d6887-113">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="d6887-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6887-114">PARAMETERS</span></span>

### <span data-ttu-id="d6887-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d6887-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d6887-116">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="d6887-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="d6887-117">По умолчанию этот командлет позволяет гостевому агенту обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="d6887-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6887-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d6887-118">-ForceRerun</span></span>
<span data-ttu-id="d6887-119">Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d6887-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="d6887-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="d6887-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d6887-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="d6887-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d6887-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d6887-122">-Location</span></span>
<span data-ttu-id="d6887-123">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6887-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d6887-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6887-124">-Name</span></span>
<span data-ttu-id="d6887-125">Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6887-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6887-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6887-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6887-127">Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="d6887-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="d6887-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d6887-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="d6887-129">Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d6887-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6887-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="d6887-130">-VMName</span></span>
<span data-ttu-id="d6887-131">Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="d6887-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6887-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6887-132">-Confirm</span></span>
<span data-ttu-id="d6887-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6887-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6887-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6887-134">-WhatIf</span></span>
<span data-ttu-id="d6887-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6887-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d6887-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6887-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6887-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6887-137">CommonParameters</span></span>
<span data-ttu-id="d6887-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6887-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6887-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6887-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6887-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6887-140">INPUTS</span></span>

### <span data-ttu-id="d6887-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6887-141">None</span></span>
<span data-ttu-id="d6887-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d6887-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6887-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6887-143">OUTPUTS</span></span>

## <span data-ttu-id="d6887-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6887-144">NOTES</span></span>

## <span data-ttu-id="d6887-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6887-145">RELATED LINKS</span></span>

