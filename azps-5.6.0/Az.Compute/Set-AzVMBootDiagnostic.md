---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: a163854838dcb8e41b7a8b65d1be9e1aca088d55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990436"
---
# <span data-ttu-id="fd147-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fd147-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="fd147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd147-102">SYNOPSIS</span></span>
<span data-ttu-id="fd147-103">Изменяет свойства диагностики загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd147-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="fd147-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd147-104">SYNTAX</span></span>

### <span data-ttu-id="fd147-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fd147-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd147-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fd147-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd147-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd147-107">DESCRIPTION</span></span>
<span data-ttu-id="fd147-108">С **помощью cmdlet Cmdlet Set-AzVMBootDiagnostic** можно настроить диагностические свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd147-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="fd147-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd147-109">EXAMPLES</span></span>

### <span data-ttu-id="fd147-110">Пример 1. Включить диагностику загрузки</span><span class="sxs-lookup"><span data-stu-id="fd147-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="fd147-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="fd147-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="fd147-112">Команда сохраняет ее в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="fd147-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="fd147-113">Вторая команда включает диагностику загрузки виртуальной машины в $VM.</span><span class="sxs-lookup"><span data-stu-id="fd147-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="fd147-114">Диагностические данные хранятся в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fd147-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="fd147-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd147-115">PARAMETERS</span></span>

### <span data-ttu-id="fd147-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd147-116">-DefaultProfile</span></span>
<span data-ttu-id="fd147-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd147-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd147-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="fd147-118">-Disable</span></span>
<span data-ttu-id="fd147-119">Указывает на то, что этот cmdlet отключает диагностику загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd147-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="fd147-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="fd147-120">-Enable</span></span>
<span data-ttu-id="fd147-121">Указывает на то, что этот cmdlet включает диагностику загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd147-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="fd147-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd147-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd147-123">Имя группы ресурсов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fd147-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="fd147-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fd147-124">-StorageAccountName</span></span>
<span data-ttu-id="fd147-125">Указывает имя учетной записи хранения, в которой нужно сохранить диагностические данные загрузки.</span><span class="sxs-lookup"><span data-stu-id="fd147-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="fd147-126">-VM</span><span class="sxs-lookup"><span data-stu-id="fd147-126">-VM</span></span>
<span data-ttu-id="fd147-127">Указывает виртуальную машину, для которой этот cmdlet изменяет диагностику загрузки.</span><span class="sxs-lookup"><span data-stu-id="fd147-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="fd147-128">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="fd147-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="fd147-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd147-129">CommonParameters</span></span>
<span data-ttu-id="fd147-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd147-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd147-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd147-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd147-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd147-132">INPUTS</span></span>

### <span data-ttu-id="fd147-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="fd147-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fd147-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fd147-134">System.String</span></span>

## <span data-ttu-id="fd147-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd147-135">OUTPUTS</span></span>

### <span data-ttu-id="fd147-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="fd147-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fd147-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd147-137">NOTES</span></span>

## <span data-ttu-id="fd147-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd147-138">RELATED LINKS</span></span>

[<span data-ttu-id="fd147-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd147-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fd147-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="fd147-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


