---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: d49fae13c69e194f0b31c702670639ce486dad81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731237"
---
# <span data-ttu-id="655d8-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="655d8-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="655d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="655d8-102">SYNOPSIS</span></span>
<span data-ttu-id="655d8-103">Добавляет расширение BGInfo к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="655d8-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="655d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="655d8-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="655d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="655d8-105">DESCRIPTION</span></span>
<span data-ttu-id="655d8-106">Командлет **Set-AzVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="655d8-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="655d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="655d8-107">EXAMPLES</span></span>

### <span data-ttu-id="655d8-108">Пример 1: Добавление расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="655d8-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="655d8-109">Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="655d8-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="655d8-110">Команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="655d8-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="655d8-111">Команда задает имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="655d8-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="655d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="655d8-112">PARAMETERS</span></span>

### <span data-ttu-id="655d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655d8-113">-DefaultProfile</span></span>
<span data-ttu-id="655d8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="655d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="655d8-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="655d8-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="655d8-116">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="655d8-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="655d8-117">По умолчанию этот командлет позволяет гостевому агенту обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="655d8-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="655d8-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="655d8-118">-ForceRerun</span></span>
<span data-ttu-id="655d8-119">Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="655d8-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="655d8-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="655d8-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="655d8-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="655d8-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="655d8-122">-Location</span><span class="sxs-lookup"><span data-stu-id="655d8-122">-Location</span></span>
<span data-ttu-id="655d8-123">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="655d8-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="655d8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="655d8-124">-Name</span></span>
<span data-ttu-id="655d8-125">Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="655d8-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="655d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="655d8-127">Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="655d8-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="655d8-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="655d8-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="655d8-129">Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="655d8-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="655d8-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="655d8-130">-VMName</span></span>
<span data-ttu-id="655d8-131">Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="655d8-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="655d8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="655d8-132">-Confirm</span></span>
<span data-ttu-id="655d8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="655d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="655d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="655d8-134">-WhatIf</span></span>
<span data-ttu-id="655d8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="655d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="655d8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="655d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="655d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655d8-137">CommonParameters</span></span>
<span data-ttu-id="655d8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="655d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655d8-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="655d8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655d8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="655d8-140">INPUTS</span></span>

### <span data-ttu-id="655d8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="655d8-141">System.String</span></span>

### <span data-ttu-id="655d8-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="655d8-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="655d8-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="655d8-143">OUTPUTS</span></span>

### <span data-ttu-id="655d8-144">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="655d8-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="655d8-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="655d8-145">NOTES</span></span>

## <span data-ttu-id="655d8-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="655d8-146">RELATED LINKS</span></span>
