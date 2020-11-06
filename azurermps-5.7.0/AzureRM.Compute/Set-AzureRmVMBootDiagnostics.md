---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561892"
---
# <span data-ttu-id="4f98e-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f98e-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="4f98e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f98e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f98e-103">Изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f98e-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f98e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f98e-104">SYNTAX</span></span>

### <span data-ttu-id="4f98e-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f98e-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f98e-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f98e-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="4f98e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f98e-107">DESCRIPTION</span></span>
<span data-ttu-id="4f98e-108">Командлет **Set-AzureRmVMBootDiagnostics** изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f98e-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="4f98e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f98e-109">EXAMPLES</span></span>

### <span data-ttu-id="4f98e-110">Пример 1: включение диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="4f98e-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="4f98e-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="4f98e-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="4f98e-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="4f98e-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="4f98e-113">Вторая команда включает диагностику загрузки для виртуальной машины в $VM.</span><span class="sxs-lookup"><span data-stu-id="4f98e-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="4f98e-114">Диагностические данные хранятся в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4f98e-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="4f98e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f98e-115">PARAMETERS</span></span>

### <span data-ttu-id="4f98e-116">-Отключение</span><span class="sxs-lookup"><span data-stu-id="4f98e-116">-Disable</span></span>
<span data-ttu-id="4f98e-117">Указывает, что этот командлет отключает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f98e-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f98e-118">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="4f98e-118">-Enable</span></span>
<span data-ttu-id="4f98e-119">Указывает на то, что этот командлет включает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f98e-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f98e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f98e-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f98e-121">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f98e-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f98e-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f98e-122">-StorageAccountName</span></span>
<span data-ttu-id="4f98e-123">Указывает имя учетной записи хранения, в которой нужно сохранить данные диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="4f98e-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f98e-124">-VM</span><span class="sxs-lookup"><span data-stu-id="4f98e-124">-VM</span></span>
<span data-ttu-id="4f98e-125">Указывает виртуальную машину, для которой этот командлет изменяет диагностику загрузки.</span><span class="sxs-lookup"><span data-stu-id="4f98e-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="4f98e-126">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="4f98e-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f98e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f98e-127">CommonParameters</span></span>
<span data-ttu-id="4f98e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f98e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f98e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f98e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f98e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f98e-130">INPUTS</span></span>

### <span data-ttu-id="4f98e-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="4f98e-131">None</span></span>
<span data-ttu-id="4f98e-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4f98e-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f98e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f98e-133">OUTPUTS</span></span>

## <span data-ttu-id="4f98e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f98e-134">NOTES</span></span>

## <span data-ttu-id="4f98e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f98e-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f98e-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4f98e-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4f98e-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4f98e-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


