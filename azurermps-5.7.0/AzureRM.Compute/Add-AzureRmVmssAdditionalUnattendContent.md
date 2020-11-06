---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561919"
---
# <span data-ttu-id="9c9ec-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="9c9ec-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="9c9ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9ec-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c9ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c9ec-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c9ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9c9ec-106">Командлет **Add-AzureRmVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="9c9ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="9c9ec-108">Пример 1: Добавление сведений в файл ответов для автоматической установки Windows</span><span class="sxs-lookup"><span data-stu-id="9c9ec-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="9c9ec-109">Эта команда добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="9c9ec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="9c9ec-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="9c9ec-111">-ComponentName</span></span>
<span data-ttu-id="9c9ec-112">Указывает имя компонента, для которого нужно настроить добавленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="9c9ec-113">Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="9c9ec-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="9c9ec-114">-Content</span></span>
<span data-ttu-id="9c9ec-115">Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="9c9ec-116">-PassName</span><span class="sxs-lookup"><span data-stu-id="9c9ec-116">-PassName</span></span>
<span data-ttu-id="9c9ec-117">Указывает имя прохода, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="9c9ec-118">Единственным допустимым значением является значение oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-118">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="9c9ec-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="9c9ec-119">-SettingName</span></span>
<span data-ttu-id="9c9ec-120">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="9c9ec-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c9ec-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="9c9ec-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="9c9ec-122">FirstLogonCommands</span></span>
- <span data-ttu-id="9c9ec-123">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="9c9ec-123">AutoLogon</span></span>

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

### <span data-ttu-id="9c9ec-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9c9ec-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9c9ec-125">Укажите объект для **установления масштаба** виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="9c9ec-126">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="9c9ec-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9c9ec-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c9ec-127">-Confirm</span></span>
<span data-ttu-id="9c9ec-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9ec-129">-WhatIf</span></span>
<span data-ttu-id="9c9ec-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c9ec-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9ec-132">CommonParameters</span></span>
<span data-ttu-id="9c9ec-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9ec-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9ec-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c9ec-135">INPUTS</span></span>

### <span data-ttu-id="9c9ec-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c9ec-136">None</span></span>
<span data-ttu-id="9c9ec-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c9ec-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9ec-138">OUTPUTS</span></span>

## <span data-ttu-id="9c9ec-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c9ec-139">NOTES</span></span>

## <span data-ttu-id="9c9ec-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c9ec-140">RELATED LINKS</span></span>

[<span data-ttu-id="9c9ec-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9c9ec-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
