---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566221"
---
# <span data-ttu-id="3ce53-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ce53-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="3ce53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ce53-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce53-103">Добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ce53-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ce53-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce53-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce53-106">Командлет **Add-AzureRmVmssDiagnosticsExtension** добавляет расширение диагностики к экземпляру "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="3ce53-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3ce53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ce53-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce53-108">Пример 1: Добавление расширения диагностики в VMSS</span><span class="sxs-lookup"><span data-stu-id="3ce53-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="3ce53-109">Эта команда добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ce53-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="3ce53-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ce53-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce53-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3ce53-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3ce53-112">Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="3ce53-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce53-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ce53-113">-Force</span></span>
<span data-ttu-id="3ce53-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ce53-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ce53-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ce53-115">-Name</span></span>
<span data-ttu-id="3ce53-116">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="3ce53-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce53-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="3ce53-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="3ce53-118">Задает путь к частному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ce53-118">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce53-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="3ce53-119">-SettingFilePath</span></span>
<span data-ttu-id="3ce53-120">Указывает путь к общедоступному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ce53-120">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="3ce53-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3ce53-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="3ce53-122">Указывает версию расширения, используемую для этого VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ce53-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="3ce53-123">Чтобы получить версию, выполните командлет [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) со значением Microsoft. Azure. Diagnostics для параметра *PublisherName* и IaaSDiagnostics для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="3ce53-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce53-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3ce53-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3ce53-125">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ce53-125">Specify the VMSS object.</span></span>
<span data-ttu-id="3ce53-126">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="3ce53-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce53-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ce53-127">-Confirm</span></span>
<span data-ttu-id="3ce53-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ce53-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce53-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce53-129">-WhatIf</span></span>
<span data-ttu-id="3ce53-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ce53-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce53-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ce53-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce53-132">CommonParameters</span></span>
<span data-ttu-id="3ce53-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ce53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce53-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce53-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce53-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ce53-135">INPUTS</span></span>

### <span data-ttu-id="3ce53-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ce53-136">None</span></span>
<span data-ttu-id="3ce53-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ce53-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ce53-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce53-138">OUTPUTS</span></span>

###  
<span data-ttu-id="3ce53-139">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3ce53-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3ce53-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ce53-140">NOTES</span></span>

## <span data-ttu-id="3ce53-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ce53-141">RELATED LINKS</span></span>

[<span data-ttu-id="3ce53-142">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3ce53-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="3ce53-143">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ce53-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="3ce53-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ce53-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
