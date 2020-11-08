---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078111"
---
# <span data-ttu-id="7aed0-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7aed0-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="7aed0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7aed0-102">SYNOPSIS</span></span>
<span data-ttu-id="7aed0-103">Изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7aed0-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="7aed0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7aed0-104">SYNTAX</span></span>

### <span data-ttu-id="7aed0-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7aed0-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7aed0-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7aed0-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aed0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aed0-107">DESCRIPTION</span></span>
<span data-ttu-id="7aed0-108">Командлет **Set-AzVMBootDiagnostic** изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7aed0-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="7aed0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7aed0-109">EXAMPLES</span></span>

### <span data-ttu-id="7aed0-110">Пример 1: включение диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="7aed0-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="7aed0-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="7aed0-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="7aed0-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="7aed0-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="7aed0-113">Вторая команда включает диагностику загрузки для виртуальной машины в $VM.</span><span class="sxs-lookup"><span data-stu-id="7aed0-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="7aed0-114">Диагностические данные хранятся в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7aed0-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="7aed0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7aed0-115">PARAMETERS</span></span>

### <span data-ttu-id="7aed0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aed0-116">-DefaultProfile</span></span>
<span data-ttu-id="7aed0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7aed0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aed0-118">-Отключение</span><span class="sxs-lookup"><span data-stu-id="7aed0-118">-Disable</span></span>
<span data-ttu-id="7aed0-119">Указывает, что этот командлет отключает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7aed0-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aed0-120">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="7aed0-120">-Enable</span></span>
<span data-ttu-id="7aed0-121">Указывает на то, что этот командлет включает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7aed0-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aed0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aed0-122">-ResourceGroupName</span></span>
<span data-ttu-id="7aed0-123">Указывает имя группы ресурсов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7aed0-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed0-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7aed0-124">-StorageAccountName</span></span>
<span data-ttu-id="7aed0-125">Указывает имя учетной записи хранения, в которой нужно сохранить данные диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="7aed0-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed0-126">-VM</span><span class="sxs-lookup"><span data-stu-id="7aed0-126">-VM</span></span>
<span data-ttu-id="7aed0-127">Указывает виртуальную машину, для которой этот командлет изменяет диагностику загрузки.</span><span class="sxs-lookup"><span data-stu-id="7aed0-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="7aed0-128">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7aed0-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aed0-129">CommonParameters</span></span>
<span data-ttu-id="7aed0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7aed0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aed0-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aed0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aed0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7aed0-132">INPUTS</span></span>

### <span data-ttu-id="7aed0-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7aed0-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7aed0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7aed0-134">System.String</span></span>

## <span data-ttu-id="7aed0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aed0-135">OUTPUTS</span></span>

### <span data-ttu-id="7aed0-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7aed0-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7aed0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7aed0-137">NOTES</span></span>

## <span data-ttu-id="7aed0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7aed0-138">RELATED LINKS</span></span>

[<span data-ttu-id="7aed0-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7aed0-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7aed0-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7aed0-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)

