---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406620"
---
# <span data-ttu-id="8a3c2-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a3c2-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="8a3c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3c2-103">Добавляет расширение диагностики в VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="8a3c2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a3c2-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a3c2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a3c2-105">DESCRIPTION</span></span>
<span data-ttu-id="8a3c2-106">Cmdlet **Add-AzVmssDiagnosticsExtension** добавляет расширение диагностики к экземпляру набора виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8a3c2-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8a3c2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a3c2-107">EXAMPLES</span></span>

### <span data-ttu-id="8a3c2-108">Пример 1. Добавление расширения диагностики в VMSS</span><span class="sxs-lookup"><span data-stu-id="8a3c2-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="8a3c2-109">Эта команда добавляет к VMSS добавит расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="8a3c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a3c2-110">PARAMETERS</span></span>

### <span data-ttu-id="8a3c2-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8a3c2-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8a3c2-112">Указывает, разрешает ли этот cmdlet агенту гостей Azure автоматически обновлять расширение до более новой версии.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="8a3c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3c2-113">-DefaultProfile</span></span>
<span data-ttu-id="8a3c2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a3c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a3c2-115">-Force</span></span>
<span data-ttu-id="8a3c2-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a3c2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8a3c2-117">-Name</span></span>
<span data-ttu-id="8a3c2-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="8a3c2-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="8a3c2-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="8a3c2-120">Путь к частному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="8a3c2-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="8a3c2-121">-SettingFilePath</span></span>
<span data-ttu-id="8a3c2-122">Путь к файлу общедоступных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="8a3c2-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8a3c2-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="8a3c2-124">Определяет версию расширения, используемого для этой VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="8a3c2-125">Чтобы получить версию, запустите cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) со значением Microsoft.Azure.Diagnostics для параметра *PublisherName* и IaaSDiagnostics для параметра *Type.*</span><span class="sxs-lookup"><span data-stu-id="8a3c2-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="8a3c2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a3c2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a3c2-127">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-127">Specify the VMSS object.</span></span>
<span data-ttu-id="8a3c2-128">Для создания объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="8a3c2-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="8a3c2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a3c2-129">-Confirm</span></span>
<span data-ttu-id="8a3c2-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a3c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a3c2-131">-WhatIf</span></span>
<span data-ttu-id="8a3c2-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a3c2-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a3c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3c2-134">CommonParameters</span></span>
<span data-ttu-id="8a3c2-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3c2-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a3c2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3c2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a3c2-137">INPUTS</span></span>

### <span data-ttu-id="8a3c2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a3c2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8a3c2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8a3c2-139">System.String</span></span>

### <span data-ttu-id="8a3c2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a3c2-140">System.Boolean</span></span>

## <span data-ttu-id="8a3c2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a3c2-141">OUTPUTS</span></span>

### <span data-ttu-id="8a3c2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a3c2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a3c2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a3c2-143">NOTES</span></span>

## <span data-ttu-id="8a3c2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a3c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="8a3c2-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8a3c2-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="8a3c2-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a3c2-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="8a3c2-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a3c2-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)