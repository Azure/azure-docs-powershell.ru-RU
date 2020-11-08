---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242893"
---
# <span data-ttu-id="50a0f-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="50a0f-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="50a0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="50a0f-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="50a0f-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="50a0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50a0f-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="50a0f-106">Командлет **Add-AzVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="50a0f-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="50a0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="50a0f-108">Пример 1: Добавление сведений в файл ответов для автоматической установки Windows</span><span class="sxs-lookup"><span data-stu-id="50a0f-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="50a0f-109">Эта команда добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="50a0f-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="50a0f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="50a0f-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="50a0f-111">-ComponentName</span></span>
<span data-ttu-id="50a0f-112">Указывает имя компонента, для которого нужно настроить добавленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="50a0f-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="50a0f-113">Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="50a0f-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="50a0f-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="50a0f-114">-Content</span></span>
<span data-ttu-id="50a0f-115">Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="50a0f-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="50a0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a0f-116">-DefaultProfile</span></span>
<span data-ttu-id="50a0f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50a0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a0f-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="50a0f-118">-PassName</span></span>
<span data-ttu-id="50a0f-119">Указывает имя прохода, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="50a0f-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="50a0f-120">Единственным допустимым значением является значение oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="50a0f-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="50a0f-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="50a0f-121">-SettingName</span></span>
<span data-ttu-id="50a0f-122">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="50a0f-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="50a0f-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="50a0f-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="50a0f-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="50a0f-124">FirstLogonCommands</span></span>
- <span data-ttu-id="50a0f-125">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="50a0f-125">AutoLogon</span></span>

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

### <span data-ttu-id="50a0f-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="50a0f-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="50a0f-127">Укажите объект для **установления масштаба** виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="50a0f-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="50a0f-128">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="50a0f-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="50a0f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50a0f-129">-Confirm</span></span>
<span data-ttu-id="50a0f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50a0f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a0f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a0f-131">-WhatIf</span></span>
<span data-ttu-id="50a0f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50a0f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50a0f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50a0f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a0f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a0f-134">CommonParameters</span></span>
<span data-ttu-id="50a0f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50a0f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a0f-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50a0f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a0f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50a0f-137">INPUTS</span></span>

### <span data-ttu-id="50a0f-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="50a0f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="50a0f-139">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. PassNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50a0f-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50a0f-140">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ComponentNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50a0f-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50a0f-141">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50a0f-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50a0f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="50a0f-142">System.String</span></span>

## <span data-ttu-id="50a0f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50a0f-143">OUTPUTS</span></span>

### <span data-ttu-id="50a0f-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="50a0f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="50a0f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="50a0f-145">NOTES</span></span>

## <span data-ttu-id="50a0f-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50a0f-146">RELATED LINKS</span></span>

[<span data-ttu-id="50a0f-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="50a0f-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
