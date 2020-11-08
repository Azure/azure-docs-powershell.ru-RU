---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245623"
---
# <span data-ttu-id="595a6-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="595a6-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="595a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="595a6-102">SYNOPSIS</span></span>
<span data-ttu-id="595a6-103">Получает сведения о расширении VMAccess.</span><span class="sxs-lookup"><span data-stu-id="595a6-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="595a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="595a6-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="595a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="595a6-105">DESCRIPTION</span></span>
<span data-ttu-id="595a6-106">Командлет **Get-AzVMAccessExtension** получает сведения о расширении виртуальной машины доступа к виртуальной машине (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="595a6-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="595a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="595a6-107">EXAMPLES</span></span>

### <span data-ttu-id="595a6-108">Пример 1: получение расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="595a6-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="595a6-109">Эта команда получает расширение VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="595a6-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="595a6-110">Пример 2: получение представления экземпляра расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="595a6-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="595a6-111">Эта команда получает представление экземпляра расширения VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="595a6-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="595a6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="595a6-112">PARAMETERS</span></span>

### <span data-ttu-id="595a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595a6-113">-DefaultProfile</span></span>
<span data-ttu-id="595a6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="595a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="595a6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="595a6-115">-Name</span></span>
<span data-ttu-id="595a6-116">Указывает имя расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="595a6-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="595a6-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="595a6-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595a6-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="595a6-119">-Status</span></span>
<span data-ttu-id="595a6-120">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="595a6-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595a6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="595a6-121">-VMName</span></span>
<span data-ttu-id="595a6-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="595a6-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="595a6-123">Этот командлет получает сведения о VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="595a6-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595a6-124">CommonParameters</span></span>
<span data-ttu-id="595a6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="595a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595a6-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="595a6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595a6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="595a6-127">INPUTS</span></span>

### <span data-ttu-id="595a6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="595a6-128">System.String</span></span>

### <span data-ttu-id="595a6-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="595a6-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="595a6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="595a6-130">OUTPUTS</span></span>

### <span data-ttu-id="595a6-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="595a6-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="595a6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="595a6-132">NOTES</span></span>

## <span data-ttu-id="595a6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="595a6-133">RELATED LINKS</span></span>

[<span data-ttu-id="595a6-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="595a6-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="595a6-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="595a6-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="595a6-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="595a6-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


