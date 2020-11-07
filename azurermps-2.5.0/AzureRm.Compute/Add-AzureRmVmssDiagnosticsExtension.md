---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913498"
---
# <span data-ttu-id="63e12-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e12-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="63e12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63e12-102">SYNOPSIS</span></span>
<span data-ttu-id="63e12-103">Добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e12-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63e12-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e12-105">DESCRIPTION</span></span>
<span data-ttu-id="63e12-106">Командлет **Add-AzureRmVmssDiagnosticsExtension** добавляет расширение диагностики к экземпляру "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="63e12-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="63e12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63e12-107">EXAMPLES</span></span>

### <span data-ttu-id="63e12-108">Пример 1: Добавление расширения диагностики в VMSS</span><span class="sxs-lookup"><span data-stu-id="63e12-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="63e12-109">Эта команда добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e12-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="63e12-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63e12-110">PARAMETERS</span></span>

### <span data-ttu-id="63e12-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="63e12-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="63e12-112">Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="63e12-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="63e12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e12-113">-DefaultProfile</span></span>
<span data-ttu-id="63e12-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63e12-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e12-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63e12-115">-Force</span></span>
<span data-ttu-id="63e12-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="63e12-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63e12-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63e12-117">-Name</span></span>
<span data-ttu-id="63e12-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="63e12-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="63e12-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="63e12-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="63e12-120">Задает путь к частному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="63e12-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="63e12-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="63e12-121">-SettingFilePath</span></span>
<span data-ttu-id="63e12-122">Указывает путь к общедоступному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="63e12-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="63e12-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="63e12-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="63e12-124">Указывает версию расширения, используемую для этого VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e12-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="63e12-125">Чтобы получить версию, выполните командлет [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) со значением Microsoft. Azure. Diagnostics для параметра *PublisherName* и IaaSDiagnostics для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="63e12-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="63e12-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63e12-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="63e12-127">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e12-127">Specify the VMSS object.</span></span>
<span data-ttu-id="63e12-128">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="63e12-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="63e12-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63e12-129">-Confirm</span></span>
<span data-ttu-id="63e12-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63e12-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e12-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e12-131">-WhatIf</span></span>
<span data-ttu-id="63e12-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63e12-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e12-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63e12-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e12-134">CommonParameters</span></span>
<span data-ttu-id="63e12-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63e12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e12-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e12-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e12-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63e12-137">INPUTS</span></span>

### <span data-ttu-id="63e12-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63e12-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="63e12-139">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63e12-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="63e12-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e12-140">OUTPUTS</span></span>

###  
<span data-ttu-id="63e12-141">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="63e12-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="63e12-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="63e12-142">NOTES</span></span>

## <span data-ttu-id="63e12-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63e12-143">RELATED LINKS</span></span>

[<span data-ttu-id="63e12-144">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="63e12-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="63e12-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e12-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="63e12-146">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e12-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
