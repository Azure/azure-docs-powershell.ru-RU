---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
ms.openlocfilehash: 2d0b09e60872050ff1bad98b468763f69edfa723
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914154"
---
# <span data-ttu-id="45a52-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="45a52-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="45a52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45a52-102">SYNOPSIS</span></span>
<span data-ttu-id="45a52-103">Добавляет расширение BGInfo к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="45a52-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45a52-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45a52-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a52-105">DESCRIPTION</span></span>
<span data-ttu-id="45a52-106">Командлет **Set-AzureRmVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="45a52-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="45a52-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45a52-107">EXAMPLES</span></span>

### <span data-ttu-id="45a52-108">Пример 1: Добавление расширения BGInfo для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="45a52-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="45a52-109">Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="45a52-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="45a52-110">Команда определяет группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45a52-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="45a52-111">Команда задает имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="45a52-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="45a52-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45a52-112">PARAMETERS</span></span>

### <span data-ttu-id="45a52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a52-113">-DefaultProfile</span></span>
<span data-ttu-id="45a52-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45a52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a52-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="45a52-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="45a52-116">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="45a52-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="45a52-117">По умолчанию этот командлет позволяет гостевому агенту обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="45a52-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="45a52-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="45a52-118">-ForceRerun</span></span>
<span data-ttu-id="45a52-119">Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="45a52-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="45a52-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="45a52-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="45a52-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="45a52-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="45a52-122">-Location</span><span class="sxs-lookup"><span data-stu-id="45a52-122">-Location</span></span>
<span data-ttu-id="45a52-123">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45a52-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="45a52-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45a52-124">-Name</span></span>
<span data-ttu-id="45a52-125">Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45a52-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="45a52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a52-126">-ResourceGroupName</span></span>
<span data-ttu-id="45a52-127">Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.</span><span class="sxs-lookup"><span data-stu-id="45a52-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="45a52-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="45a52-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="45a52-129">Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="45a52-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="45a52-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="45a52-130">-VMName</span></span>
<span data-ttu-id="45a52-131">Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.</span><span class="sxs-lookup"><span data-stu-id="45a52-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="45a52-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45a52-132">-Confirm</span></span>
<span data-ttu-id="45a52-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45a52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a52-134">-WhatIf</span></span>
<span data-ttu-id="45a52-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45a52-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="45a52-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45a52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a52-137">CommonParameters</span></span>
<span data-ttu-id="45a52-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45a52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a52-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a52-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a52-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45a52-140">INPUTS</span></span>

### <span data-ttu-id="45a52-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="45a52-141">None</span></span>
<span data-ttu-id="45a52-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="45a52-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45a52-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a52-143">OUTPUTS</span></span>

### <span data-ttu-id="45a52-144">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="45a52-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="45a52-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="45a52-145">NOTES</span></span>

## <span data-ttu-id="45a52-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45a52-146">RELATED LINKS</span></span>

