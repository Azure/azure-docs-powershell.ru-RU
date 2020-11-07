---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 21b8b73d1063881104b799c016c2cfab618a9705
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911349"
---
# <span data-ttu-id="71c88-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="71c88-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="71c88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71c88-102">SYNOPSIS</span></span>
<span data-ttu-id="71c88-103">Добавляет расширение BGInfo к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="71c88-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="71c88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71c88-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71c88-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71c88-105">DESCRIPTION</span></span>
<span data-ttu-id="71c88-106">Командлет **Set-AzVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="71c88-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="71c88-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71c88-107">EXAMPLES</span></span>

### <span data-ttu-id="71c88-108">Пример 1: Добавление расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="71c88-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="71c88-109">Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="71c88-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="71c88-110">Команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c88-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="71c88-111">Команда задает имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="71c88-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="71c88-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71c88-112">PARAMETERS</span></span>

### <span data-ttu-id="71c88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c88-113">-DefaultProfile</span></span>
<span data-ttu-id="71c88-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71c88-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c88-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="71c88-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="71c88-116">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="71c88-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="71c88-117">По умолчанию этот командлет позволяет гостевому агенту обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="71c88-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="71c88-118">-ForceRerun</span></span>
<span data-ttu-id="71c88-119">Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="71c88-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="71c88-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="71c88-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="71c88-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="71c88-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-122">-Location</span><span class="sxs-lookup"><span data-stu-id="71c88-122">-Location</span></span>
<span data-ttu-id="71c88-123">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c88-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71c88-124">-Name</span></span>
<span data-ttu-id="71c88-125">Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c88-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c88-126">-ResourceGroupName</span></span>
<span data-ttu-id="71c88-127">Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="71c88-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="71c88-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="71c88-129">Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="71c88-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="71c88-130">-VMName</span></span>
<span data-ttu-id="71c88-131">Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="71c88-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c88-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71c88-132">-Confirm</span></span>
<span data-ttu-id="71c88-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71c88-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c88-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c88-134">-WhatIf</span></span>
<span data-ttu-id="71c88-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71c88-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="71c88-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71c88-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c88-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c88-137">CommonParameters</span></span>
<span data-ttu-id="71c88-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71c88-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c88-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c88-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c88-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71c88-140">INPUTS</span></span>

### <span data-ttu-id="71c88-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="71c88-141">None</span></span>
<span data-ttu-id="71c88-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="71c88-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71c88-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71c88-143">OUTPUTS</span></span>

### <span data-ttu-id="71c88-144">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71c88-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="71c88-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="71c88-145">NOTES</span></span>

## <span data-ttu-id="71c88-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71c88-146">RELATED LINKS</span></span>

