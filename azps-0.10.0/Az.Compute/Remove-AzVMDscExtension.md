---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911411"
---
# <span data-ttu-id="30c79-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="30c79-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="30c79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30c79-102">SYNOPSIS</span></span>
<span data-ttu-id="30c79-103">Удаляет обработчик расширений DSC из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30c79-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="30c79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30c79-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c79-105">DESCRIPTION</span></span>
<span data-ttu-id="30c79-106">Командлет **Remove-AzVMDscExtension** удаляет обработчик расширения нужной конфигурации состояния (DSC) из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30c79-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="30c79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30c79-107">EXAMPLES</span></span>

### <span data-ttu-id="30c79-108">Пример 1: удаление расширения DSC</span><span class="sxs-lookup"><span data-stu-id="30c79-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="30c79-109">Эта команда удаляет расширение с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="30c79-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="30c79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30c79-110">PARAMETERS</span></span>

### <span data-ttu-id="30c79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c79-111">-DefaultProfile</span></span>
<span data-ttu-id="30c79-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30c79-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c79-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30c79-113">-Name</span></span>
<span data-ttu-id="30c79-114">Указывает имя расширения DSC, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="30c79-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="30c79-115">Командлет Set-AzVMDscExtension задает это имя в Microsoft. PowerShell. DSC, которое является значением по умолчанию, используемым функцией **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="30c79-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="30c79-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c79-116">-ResourceGroupName</span></span>
<span data-ttu-id="30c79-117">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30c79-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="30c79-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="30c79-118">-VMName</span></span>
<span data-ttu-id="30c79-119">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="30c79-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="30c79-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30c79-120">-Confirm</span></span>
<span data-ttu-id="30c79-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30c79-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c79-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c79-122">-WhatIf</span></span>
<span data-ttu-id="30c79-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30c79-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="30c79-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30c79-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c79-125">CommonParameters</span></span>
<span data-ttu-id="30c79-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30c79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c79-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c79-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c79-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30c79-128">INPUTS</span></span>

### <span data-ttu-id="30c79-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="30c79-129">None</span></span>
<span data-ttu-id="30c79-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="30c79-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30c79-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c79-131">OUTPUTS</span></span>

### <span data-ttu-id="30c79-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="30c79-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="30c79-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="30c79-133">NOTES</span></span>

## <span data-ttu-id="30c79-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30c79-134">RELATED LINKS</span></span>

[<span data-ttu-id="30c79-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="30c79-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="30c79-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="30c79-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


