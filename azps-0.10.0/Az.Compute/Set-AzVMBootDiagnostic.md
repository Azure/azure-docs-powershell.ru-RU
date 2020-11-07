---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: e3e03083e831f38143423e69c84a67bfbc0440db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911348"
---
# <span data-ttu-id="62f6c-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="62f6c-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="62f6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="62f6c-103">Изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62f6c-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="62f6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62f6c-104">SYNTAX</span></span>

### <span data-ttu-id="62f6c-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="62f6c-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f6c-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="62f6c-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62f6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62f6c-107">DESCRIPTION</span></span>
<span data-ttu-id="62f6c-108">Командлет **Set-AzVMBootDiagnostic** изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62f6c-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="62f6c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62f6c-109">EXAMPLES</span></span>

### <span data-ttu-id="62f6c-110">Пример 1: включение диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="62f6c-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="62f6c-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="62f6c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="62f6c-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="62f6c-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="62f6c-113">Вторая команда включает диагностику загрузки для виртуальной машины в $VM.</span><span class="sxs-lookup"><span data-stu-id="62f6c-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="62f6c-114">Диагностические данные хранятся в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="62f6c-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="62f6c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62f6c-115">PARAMETERS</span></span>

### <span data-ttu-id="62f6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f6c-116">-DefaultProfile</span></span>
<span data-ttu-id="62f6c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62f6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f6c-118">-Отключение</span><span class="sxs-lookup"><span data-stu-id="62f6c-118">-Disable</span></span>
<span data-ttu-id="62f6c-119">Указывает, что этот командлет отключает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62f6c-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="62f6c-120">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="62f6c-120">-Enable</span></span>
<span data-ttu-id="62f6c-121">Указывает на то, что этот командлет включает диагностику загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62f6c-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="62f6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="62f6c-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62f6c-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62f6c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62f6c-124">-StorageAccountName</span></span>
<span data-ttu-id="62f6c-125">Указывает имя учетной записи хранения, в которой нужно сохранить данные диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="62f6c-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="62f6c-126">-VM</span><span class="sxs-lookup"><span data-stu-id="62f6c-126">-VM</span></span>
<span data-ttu-id="62f6c-127">Указывает виртуальную машину, для которой этот командлет изменяет диагностику загрузки.</span><span class="sxs-lookup"><span data-stu-id="62f6c-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="62f6c-128">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="62f6c-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="62f6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f6c-129">CommonParameters</span></span>
<span data-ttu-id="62f6c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62f6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f6c-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f6c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f6c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62f6c-132">INPUTS</span></span>

### <span data-ttu-id="62f6c-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="62f6c-133">PSVirtualMachine</span></span>
<span data-ttu-id="62f6c-134">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="62f6c-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="62f6c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62f6c-135">OUTPUTS</span></span>

### <span data-ttu-id="62f6c-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="62f6c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="62f6c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="62f6c-137">NOTES</span></span>

## <span data-ttu-id="62f6c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62f6c-138">RELATED LINKS</span></span>

[<span data-ttu-id="62f6c-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="62f6c-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="62f6c-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="62f6c-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


