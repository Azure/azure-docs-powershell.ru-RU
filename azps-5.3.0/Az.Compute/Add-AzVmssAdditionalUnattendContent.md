---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509250"
---
# <span data-ttu-id="6c758-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="6c758-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="6c758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c758-102">SYNOPSIS</span></span>
<span data-ttu-id="6c758-103">Добавляет сведения в неотвеченный файл ответа на установку Windows.</span><span class="sxs-lookup"><span data-stu-id="6c758-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6c758-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c758-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c758-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c758-105">DESCRIPTION</span></span>
<span data-ttu-id="6c758-106">Для получения сведений в файле ответа на вопросы о настройке Windows дополнительный файл данных добавляется с его начертанием **Add-AzVmssAdditionalUnattendContent.**</span><span class="sxs-lookup"><span data-stu-id="6c758-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6c758-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c758-107">EXAMPLES</span></span>

### <span data-ttu-id="6c758-108">Пример 1. Добавление сведений в файл ответа на вопросы о настройке Windows</span><span class="sxs-lookup"><span data-stu-id="6c758-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="6c758-109">Эта команда добавляет сведения в несмежный файл ответа на запрос программы установки Windows.</span><span class="sxs-lookup"><span data-stu-id="6c758-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6c758-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c758-110">PARAMETERS</span></span>

### <span data-ttu-id="6c758-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="6c758-111">-ComponentName</span></span>
<span data-ttu-id="6c758-112">Имя компонента, который нужно настроить с добавленным контентом.</span><span class="sxs-lookup"><span data-stu-id="6c758-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="6c758-113">Допустимым является только microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="6c758-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="6c758-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="6c758-114">-Content</span></span>
<span data-ttu-id="6c758-115">Определяет содержимое в формате XML, которое добавляется в unattend.xml указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="6c758-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="6c758-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c758-116">-DefaultProfile</span></span>
<span data-ttu-id="6c758-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c758-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c758-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="6c758-118">-PassName</span></span>
<span data-ttu-id="6c758-119">Указывает имя передать, к какому содержимому применяется.</span><span class="sxs-lookup"><span data-stu-id="6c758-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="6c758-120">Единственное допустимое значение — oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="6c758-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="6c758-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="6c758-121">-SettingName</span></span>
<span data-ttu-id="6c758-122">Определяет имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="6c758-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="6c758-123">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="6c758-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="6c758-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="6c758-124">FirstLogonCommands</span></span>
- <span data-ttu-id="6c758-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="6c758-125">AutoLogon</span></span>

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

### <span data-ttu-id="6c758-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c758-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6c758-127">Укажите объект набора **масштаба виртуальной машины.**</span><span class="sxs-lookup"><span data-stu-id="6c758-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="6c758-128">Для создания объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="6c758-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6c758-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c758-129">-Confirm</span></span>
<span data-ttu-id="6c758-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c758-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c758-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c758-131">-WhatIf</span></span>
<span data-ttu-id="6c758-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c758-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c758-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c758-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c758-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c758-134">CommonParameters</span></span>
<span data-ttu-id="6c758-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c758-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c758-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c758-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c758-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c758-137">INPUTS</span></span>

### <span data-ttu-id="6c758-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c758-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6c758-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6c758-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6c758-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6c758-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6c758-141">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6c758-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6c758-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6c758-142">System.String</span></span>

## <span data-ttu-id="6c758-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c758-143">OUTPUTS</span></span>

### <span data-ttu-id="6c758-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c758-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6c758-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c758-145">NOTES</span></span>

## <span data-ttu-id="6c758-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c758-146">RELATED LINKS</span></span>

[<span data-ttu-id="6c758-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6c758-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
