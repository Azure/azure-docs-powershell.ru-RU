---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312041"
---
# <span data-ttu-id="54663-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="54663-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="54663-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54663-102">SYNOPSIS</span></span>
<span data-ttu-id="54663-103">Добавляет расширение BGInfo к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="54663-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="54663-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54663-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54663-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54663-105">DESCRIPTION</span></span>
<span data-ttu-id="54663-106">Командлет **Set-AzVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="54663-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="54663-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54663-107">EXAMPLES</span></span>

### <span data-ttu-id="54663-108">Пример 1: Добавление расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="54663-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="54663-109">Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="54663-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="54663-110">Команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54663-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="54663-111">Команда задает имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="54663-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="54663-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54663-112">PARAMETERS</span></span>

### <span data-ttu-id="54663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54663-113">-DefaultProfile</span></span>
<span data-ttu-id="54663-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54663-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54663-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="54663-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="54663-116">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="54663-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="54663-117">По умолчанию этот командлет позволяет гостевому агенту обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="54663-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="54663-118">-ForceRerun</span></span>
<span data-ttu-id="54663-119">Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="54663-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="54663-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="54663-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="54663-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="54663-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-122">-Location</span><span class="sxs-lookup"><span data-stu-id="54663-122">-Location</span></span>
<span data-ttu-id="54663-123">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54663-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54663-124">-Name</span></span>
<span data-ttu-id="54663-125">Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54663-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="54663-126">-NoWait</span></span>
<span data-ttu-id="54663-127">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="54663-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="54663-128">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="54663-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54663-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54663-129">-ResourceGroupName</span></span>
<span data-ttu-id="54663-130">Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="54663-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="54663-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="54663-132">Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="54663-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="54663-133">-VMName</span></span>
<span data-ttu-id="54663-134">Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="54663-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54663-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54663-135">-Confirm</span></span>
<span data-ttu-id="54663-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54663-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54663-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54663-137">-WhatIf</span></span>
<span data-ttu-id="54663-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54663-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54663-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54663-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54663-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54663-140">CommonParameters</span></span>
<span data-ttu-id="54663-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54663-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54663-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54663-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54663-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54663-143">INPUTS</span></span>

### <span data-ttu-id="54663-144">System. String</span><span class="sxs-lookup"><span data-stu-id="54663-144">System.String</span></span>

### <span data-ttu-id="54663-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54663-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54663-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54663-146">OUTPUTS</span></span>

### <span data-ttu-id="54663-147">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="54663-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="54663-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="54663-148">NOTES</span></span>

## <span data-ttu-id="54663-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54663-149">RELATED LINKS</span></span>
