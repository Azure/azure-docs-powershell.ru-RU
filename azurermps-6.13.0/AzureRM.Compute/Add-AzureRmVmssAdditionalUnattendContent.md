---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: 6100a8594b380981bfbfbe25f2334740e915ff2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733167"
---
# <span data-ttu-id="27eab-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="27eab-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="27eab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27eab-102">SYNOPSIS</span></span>
<span data-ttu-id="27eab-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="27eab-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27eab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27eab-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27eab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27eab-105">DESCRIPTION</span></span>
<span data-ttu-id="27eab-106">Командлет **Add-AzureRmVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="27eab-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="27eab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27eab-107">EXAMPLES</span></span>

### <span data-ttu-id="27eab-108">Пример 1: Добавление сведений в файл ответов для автоматической установки Windows</span><span class="sxs-lookup"><span data-stu-id="27eab-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="27eab-109">Эта команда добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="27eab-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="27eab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27eab-110">PARAMETERS</span></span>

### <span data-ttu-id="27eab-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="27eab-111">-ComponentName</span></span>
<span data-ttu-id="27eab-112">Указывает имя компонента, для которого нужно настроить добавленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="27eab-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="27eab-113">Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="27eab-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="27eab-114">-Content</span></span>
<span data-ttu-id="27eab-115">Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="27eab-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27eab-116">-DefaultProfile</span></span>
<span data-ttu-id="27eab-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27eab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="27eab-118">-PassName</span></span>
<span data-ttu-id="27eab-119">Указывает имя прохода, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="27eab-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="27eab-120">Единственным допустимым значением является значение oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="27eab-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="27eab-121">-SettingName</span></span>
<span data-ttu-id="27eab-122">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="27eab-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="27eab-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="27eab-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="27eab-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="27eab-124">FirstLogonCommands</span></span>
- <span data-ttu-id="27eab-125">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="27eab-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27eab-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="27eab-127">Укажите объект для **установления масштаба** виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="27eab-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="27eab-128">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="27eab-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="27eab-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27eab-129">-Confirm</span></span>
<span data-ttu-id="27eab-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27eab-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27eab-131">-WhatIf</span></span>
<span data-ttu-id="27eab-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27eab-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27eab-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27eab-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27eab-134">CommonParameters</span></span>
<span data-ttu-id="27eab-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27eab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27eab-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27eab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27eab-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27eab-137">INPUTS</span></span>

### <span data-ttu-id="27eab-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27eab-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="27eab-139">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. PassNames, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="27eab-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="27eab-140">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ComponentNames, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="27eab-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="27eab-141">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="27eab-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="27eab-142">System. String</span><span class="sxs-lookup"><span data-stu-id="27eab-142">System.String</span></span>

## <span data-ttu-id="27eab-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27eab-143">OUTPUTS</span></span>

### <span data-ttu-id="27eab-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27eab-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="27eab-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="27eab-145">NOTES</span></span>

## <span data-ttu-id="27eab-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27eab-146">RELATED LINKS</span></span>

[<span data-ttu-id="27eab-147">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="27eab-147">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
