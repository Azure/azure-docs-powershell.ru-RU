---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b3e9f8703b2130426d98a4a59fe25eb2f3f8fbdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557543"
---
# <span data-ttu-id="be0cc-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be0cc-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="be0cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="be0cc-103">Удаляет обработчик расширений DSC из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be0cc-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be0cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be0cc-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be0cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="be0cc-106">Командлет **Remove-AzureRmVMDscExtension** удаляет обработчик расширения нужной конфигурации состояния (DSC) из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be0cc-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="be0cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="be0cc-108">Пример 1: удаление расширения DSC</span><span class="sxs-lookup"><span data-stu-id="be0cc-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="be0cc-109">Эта команда удаляет расширение с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="be0cc-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="be0cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be0cc-110">PARAMETERS</span></span>

### <span data-ttu-id="be0cc-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be0cc-111">-Name</span></span>
<span data-ttu-id="be0cc-112">Указывает имя расширения DSC, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be0cc-112">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="be0cc-113">Командлет Set-AzureRmVMDscExtension задает это имя в Microsoft. PowerShell. DSC, которое является значением по умолчанию, используемым функцией **Remove-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="be0cc-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="be0cc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0cc-114">-ResourceGroupName</span></span>
<span data-ttu-id="be0cc-115">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be0cc-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="be0cc-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="be0cc-116">-VMName</span></span>
<span data-ttu-id="be0cc-117">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="be0cc-117">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="be0cc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be0cc-118">-Confirm</span></span>
<span data-ttu-id="be0cc-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be0cc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be0cc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be0cc-120">-WhatIf</span></span>
<span data-ttu-id="be0cc-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be0cc-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="be0cc-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be0cc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be0cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0cc-123">CommonParameters</span></span>
<span data-ttu-id="be0cc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be0cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0cc-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0cc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0cc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be0cc-126">INPUTS</span></span>

### <span data-ttu-id="be0cc-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="be0cc-127">None</span></span>
<span data-ttu-id="be0cc-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="be0cc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be0cc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be0cc-129">OUTPUTS</span></span>

## <span data-ttu-id="be0cc-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="be0cc-130">NOTES</span></span>

## <span data-ttu-id="be0cc-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be0cc-131">RELATED LINKS</span></span>

[<span data-ttu-id="be0cc-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be0cc-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="be0cc-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be0cc-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


