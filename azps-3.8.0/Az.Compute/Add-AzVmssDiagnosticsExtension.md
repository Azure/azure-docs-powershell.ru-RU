---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074904"
---
# <span data-ttu-id="c8d34-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8d34-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="c8d34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8d34-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d34-103">Добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8d34-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="c8d34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8d34-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d34-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d34-106">Командлет **Add-AzVmssDiagnosticsExtension** добавляет расширение диагностики к экземпляру "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="c8d34-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c8d34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8d34-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d34-108">Пример 1: Добавление расширения диагностики в VMSS</span><span class="sxs-lookup"><span data-stu-id="c8d34-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="c8d34-109">Эта команда добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8d34-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="c8d34-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8d34-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d34-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c8d34-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c8d34-112">Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="c8d34-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d34-113">-DefaultProfile</span></span>
<span data-ttu-id="c8d34-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d34-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8d34-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c8d34-115">-Force</span></span>
<span data-ttu-id="c8d34-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8d34-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8d34-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8d34-117">-Name</span></span>
<span data-ttu-id="c8d34-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="c8d34-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="c8d34-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="c8d34-120">Задает путь к частному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c8d34-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="c8d34-121">-SettingFilePath</span></span>
<span data-ttu-id="c8d34-122">Указывает путь к общедоступному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c8d34-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c8d34-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="c8d34-124">Указывает версию расширения, используемую для этого VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8d34-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="c8d34-125">Чтобы получить версию, выполните командлет [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) со значением Microsoft. Azure. Diagnostics для параметра *PublisherName* и IaaSDiagnostics для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="c8d34-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8d34-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8d34-127">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8d34-127">Specify the VMSS object.</span></span>
<span data-ttu-id="c8d34-128">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d34-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d34-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8d34-129">-Confirm</span></span>
<span data-ttu-id="c8d34-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d34-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d34-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d34-131">-WhatIf</span></span>
<span data-ttu-id="c8d34-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d34-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d34-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8d34-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d34-134">CommonParameters</span></span>
<span data-ttu-id="c8d34-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8d34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d34-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8d34-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d34-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8d34-137">INPUTS</span></span>

### <span data-ttu-id="c8d34-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8d34-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c8d34-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d34-139">System.String</span></span>

### <span data-ttu-id="c8d34-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8d34-140">System.Boolean</span></span>

## <span data-ttu-id="c8d34-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d34-141">OUTPUTS</span></span>

### <span data-ttu-id="c8d34-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8d34-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c8d34-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8d34-143">NOTES</span></span>

## <span data-ttu-id="c8d34-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8d34-144">RELATED LINKS</span></span>

[<span data-ttu-id="c8d34-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c8d34-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="c8d34-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8d34-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="c8d34-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8d34-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
