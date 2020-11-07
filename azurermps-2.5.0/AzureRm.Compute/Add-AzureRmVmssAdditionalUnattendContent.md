---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: c0ceb74c6880508f04fb0832c48d0752507f5a5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913698"
---
# <span data-ttu-id="4fec2-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="4fec2-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="4fec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fec2-102">SYNOPSIS</span></span>
<span data-ttu-id="4fec2-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="4fec2-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fec2-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fec2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fec2-105">DESCRIPTION</span></span>
<span data-ttu-id="4fec2-106">Командлет **Add-AzureRmVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="4fec2-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4fec2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fec2-107">EXAMPLES</span></span>

### <span data-ttu-id="4fec2-108">Пример 1: Добавление сведений в файл ответов для автоматической установки Windows</span><span class="sxs-lookup"><span data-stu-id="4fec2-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="4fec2-109">Эта команда добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="4fec2-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4fec2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fec2-110">PARAMETERS</span></span>

### <span data-ttu-id="4fec2-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="4fec2-111">-ComponentName</span></span>
<span data-ttu-id="4fec2-112">Указывает имя компонента, для которого нужно настроить добавленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="4fec2-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="4fec2-113">Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="4fec2-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="4fec2-114">-Content</span></span>
<span data-ttu-id="4fec2-115">Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="4fec2-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fec2-116">-DefaultProfile</span></span>
<span data-ttu-id="4fec2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fec2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fec2-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="4fec2-118">-PassName</span></span>
<span data-ttu-id="4fec2-119">Указывает имя прохода, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="4fec2-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="4fec2-120">Единственным допустимым значением является значение oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="4fec2-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="4fec2-121">-SettingName</span></span>
<span data-ttu-id="4fec2-122">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="4fec2-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="4fec2-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4fec2-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="4fec2-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="4fec2-124">FirstLogonCommands</span></span>
- <span data-ttu-id="4fec2-125">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="4fec2-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fec2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4fec2-127">Укажите объект для **установления масштаба** виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4fec2-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="4fec2-128">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="4fec2-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fec2-129">-Confirm</span></span>
<span data-ttu-id="4fec2-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fec2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fec2-131">-WhatIf</span></span>
<span data-ttu-id="4fec2-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4fec2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fec2-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4fec2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fec2-134">CommonParameters</span></span>
<span data-ttu-id="4fec2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fec2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fec2-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fec2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fec2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fec2-137">INPUTS</span></span>

### <span data-ttu-id="4fec2-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fec2-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="4fec2-139">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4fec2-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="4fec2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fec2-140">OUTPUTS</span></span>

### <span data-ttu-id="4fec2-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fec2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4fec2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fec2-142">NOTES</span></span>

## <span data-ttu-id="4fec2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fec2-143">RELATED LINKS</span></span>

[<span data-ttu-id="4fec2-144">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4fec2-144">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
