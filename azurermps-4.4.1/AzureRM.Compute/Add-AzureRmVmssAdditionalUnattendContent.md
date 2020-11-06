---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: d99e54439b2e8b4474c4b0123634ddd7c286ea9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557939"
---
# <span data-ttu-id="7d054-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7d054-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="7d054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d054-102">SYNOPSIS</span></span>
<span data-ttu-id="7d054-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="7d054-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d054-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d054-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d054-105">DESCRIPTION</span></span>
<span data-ttu-id="7d054-106">Командлет **Add-AzureRmVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="7d054-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7d054-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d054-107">EXAMPLES</span></span>

### <span data-ttu-id="7d054-108">Пример 1: Добавление сведений в файл ответов для автоматической установки Windows</span><span class="sxs-lookup"><span data-stu-id="7d054-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="7d054-109">Эта команда добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="7d054-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7d054-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d054-110">PARAMETERS</span></span>

### <span data-ttu-id="7d054-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="7d054-111">-ComponentName</span></span>
<span data-ttu-id="7d054-112">Указывает имя компонента, для которого нужно настроить добавленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="7d054-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="7d054-113">Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="7d054-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="7d054-114">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="7d054-114">-Content</span></span>
<span data-ttu-id="7d054-115">Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.</span><span class="sxs-lookup"><span data-stu-id="7d054-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="7d054-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d054-116">-DefaultProfile</span></span>
<span data-ttu-id="7d054-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d054-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d054-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="7d054-118">-PassName</span></span>
<span data-ttu-id="7d054-119">Указывает имя прохода, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="7d054-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="7d054-120">Единственным допустимым значением является значение oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="7d054-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="7d054-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7d054-121">-SettingName</span></span>
<span data-ttu-id="7d054-122">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="7d054-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="7d054-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7d054-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="7d054-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="7d054-124">FirstLogonCommands</span></span>
- <span data-ttu-id="7d054-125">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="7d054-125">AutoLogon</span></span>

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

### <span data-ttu-id="7d054-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7d054-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7d054-127">Укажите объект для **установления масштаба** виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d054-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="7d054-128">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7d054-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="7d054-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d054-129">-Confirm</span></span>
<span data-ttu-id="7d054-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d054-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d054-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d054-131">-WhatIf</span></span>
<span data-ttu-id="7d054-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d054-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d054-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d054-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d054-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d054-134">CommonParameters</span></span>
<span data-ttu-id="7d054-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d054-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d054-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d054-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d054-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d054-137">INPUTS</span></span>

## <span data-ttu-id="7d054-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d054-138">OUTPUTS</span></span>

## <span data-ttu-id="7d054-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d054-139">NOTES</span></span>

## <span data-ttu-id="7d054-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d054-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d054-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7d054-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
