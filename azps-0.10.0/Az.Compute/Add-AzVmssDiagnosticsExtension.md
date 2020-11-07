---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911584"
---
# <span data-ttu-id="b83f3-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b83f3-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="b83f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b83f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b83f3-103">Добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b83f3-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b83f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b83f3-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b83f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b83f3-105">DESCRIPTION</span></span>
<span data-ttu-id="b83f3-106">Командлет **Add-AzVmssDiagnosticsExtension** добавляет расширение диагностики к экземпляру "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="b83f3-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b83f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b83f3-107">EXAMPLES</span></span>

### <span data-ttu-id="b83f3-108">Пример 1: Добавление расширения диагностики в VMSS</span><span class="sxs-lookup"><span data-stu-id="b83f3-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="b83f3-109">Эта команда добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b83f3-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b83f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b83f3-110">PARAMETERS</span></span>

### <span data-ttu-id="b83f3-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b83f3-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b83f3-112">Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="b83f3-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="b83f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83f3-113">-DefaultProfile</span></span>
<span data-ttu-id="b83f3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b83f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b83f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b83f3-115">-Force</span></span>
<span data-ttu-id="b83f3-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b83f3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b83f3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b83f3-117">-Name</span></span>
<span data-ttu-id="b83f3-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="b83f3-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="b83f3-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b83f3-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="b83f3-120">Задает путь к частному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b83f3-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="b83f3-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b83f3-121">-SettingFilePath</span></span>
<span data-ttu-id="b83f3-122">Указывает путь к общедоступному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b83f3-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="b83f3-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b83f3-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="b83f3-124">Указывает версию расширения, используемую для этого VMSS.</span><span class="sxs-lookup"><span data-stu-id="b83f3-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="b83f3-125">Чтобы получить версию, выполните командлет [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) со значением Microsoft. Azure. Diagnostics для параметра *PublisherName* и IaaSDiagnostics для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="b83f3-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="b83f3-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b83f3-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b83f3-127">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="b83f3-127">Specify the VMSS object.</span></span>
<span data-ttu-id="b83f3-128">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b83f3-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b83f3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b83f3-129">-Confirm</span></span>
<span data-ttu-id="b83f3-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b83f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b83f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b83f3-131">-WhatIf</span></span>
<span data-ttu-id="b83f3-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b83f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b83f3-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b83f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b83f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83f3-134">CommonParameters</span></span>
<span data-ttu-id="b83f3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b83f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83f3-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83f3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83f3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b83f3-137">INPUTS</span></span>

### <span data-ttu-id="b83f3-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b83f3-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b83f3-139">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b83f3-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b83f3-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b83f3-140">OUTPUTS</span></span>

###  
<span data-ttu-id="b83f3-141">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b83f3-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b83f3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b83f3-142">NOTES</span></span>

## <span data-ttu-id="b83f3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b83f3-143">RELATED LINKS</span></span>

[<span data-ttu-id="b83f3-144">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b83f3-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b83f3-145">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b83f3-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="b83f3-146">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b83f3-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
