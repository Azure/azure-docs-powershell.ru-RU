---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509034"
---
# <span data-ttu-id="3cb7c-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="3cb7c-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="3cb7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb7c-103">Добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="3cb7c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cb7c-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb7c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cb7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb7c-106">Cmdlet **Set-AzVMBGInfoExtension** добавит расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="3cb7c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cb7c-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb7c-108">Пример 1. Добавление расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="3cb7c-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="3cb7c-109">Эта команда добавляет расширение BGInfo на виртуальную машину с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="3cb7c-110">Эта команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="3cb7c-111">Эта команда определяет имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="3cb7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cb7c-112">PARAMETERS</span></span>

### <span data-ttu-id="3cb7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb7c-113">-DefaultProfile</span></span>
<span data-ttu-id="3cb7c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb7c-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3cb7c-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3cb7c-116">Указывает на то, что этот cmdlet предотвращает автоматическое обновление расширения до более новой версии с гостевых агентом Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="3cb7c-117">По умолчанию этот cmdlet позволяет агенту гостя обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="3cb7c-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3cb7c-118">-ForceRerun</span></span>
<span data-ttu-id="3cb7c-119">Указывает, что расширение должно быть повторно запускаться с тем же общедоступным или защищенным параметром.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="3cb7c-120">Значение может быть любой строкой, которая отличается от текущей.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="3cb7c-121">Если параметр forceUpdateTag не изменился, обработник по-прежнему применяет обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="3cb7c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="3cb7c-122">-Location</span></span>
<span data-ttu-id="3cb7c-123">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="3cb7c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb7c-124">-Name</span></span>
<span data-ttu-id="3cb7c-125">Указывает имя расширения BGInfo, которое этот cmdlet добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="3cb7c-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3cb7c-126">-NoWait</span></span>
<span data-ttu-id="3cb7c-127">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3cb7c-128">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3cb7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="3cb7c-130">Имя группы ресурсов виртуальной машины, к которой этот cmdlet добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="3cb7c-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3cb7c-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="3cb7c-132">Определяет версию расширения, которое этот cmdlet добавит на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="3cb7c-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="3cb7c-133">-VMName</span></span>
<span data-ttu-id="3cb7c-134">Указывает имя виртуальной машины, к которой этот cmdlet добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="3cb7c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cb7c-135">-Confirm</span></span>
<span data-ttu-id="3cb7c-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb7c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb7c-137">-WhatIf</span></span>
<span data-ttu-id="3cb7c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb7c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb7c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb7c-140">CommonParameters</span></span>
<span data-ttu-id="3cb7c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb7c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb7c-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb7c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb7c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cb7c-143">INPUTS</span></span>

### <span data-ttu-id="3cb7c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3cb7c-144">System.String</span></span>

### <span data-ttu-id="3cb7c-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cb7c-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3cb7c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cb7c-146">OUTPUTS</span></span>

### <span data-ttu-id="3cb7c-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3cb7c-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3cb7c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cb7c-148">NOTES</span></span>

## <span data-ttu-id="3cb7c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cb7c-149">RELATED LINKS</span></span>
