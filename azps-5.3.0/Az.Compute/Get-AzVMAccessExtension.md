---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509186"
---
# <span data-ttu-id="265d7-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="265d7-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="265d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="265d7-102">SYNOPSIS</span></span>
<span data-ttu-id="265d7-103">Сведения о расширении VMAccess.</span><span class="sxs-lookup"><span data-stu-id="265d7-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="265d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="265d7-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="265d7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="265d7-105">DESCRIPTION</span></span>
<span data-ttu-id="265d7-106">Cmdlet **Get-AzVMAccessExtension** получает сведения о расширении виртуальной машины (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="265d7-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="265d7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="265d7-107">EXAMPLES</span></span>

### <span data-ttu-id="265d7-108">Пример 1. Получить расширение VMAccess</span><span class="sxs-lookup"><span data-stu-id="265d7-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="265d7-109">Эта команда получает расширение VMAccess ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="265d7-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="265d7-110">Пример 2. Просмотр представления экземпляра расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="265d7-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="265d7-111">Эта команда возвращает представление экземпляра расширения VMAccess ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="265d7-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="265d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="265d7-112">PARAMETERS</span></span>

### <span data-ttu-id="265d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265d7-113">-DefaultProfile</span></span>
<span data-ttu-id="265d7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="265d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="265d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="265d7-115">-Name</span></span>
<span data-ttu-id="265d7-116">Указывает имя расширения, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="265d7-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="265d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="265d7-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="265d7-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="265d7-119">-Status</span><span class="sxs-lookup"><span data-stu-id="265d7-119">-Status</span></span>
<span data-ttu-id="265d7-120">Указывает на то, что этот cmdlet получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="265d7-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="265d7-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="265d7-121">-VMName</span></span>
<span data-ttu-id="265d7-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="265d7-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="265d7-123">Этот cmdlet получает сведения о VMAccess для виртуальной машины, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="265d7-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="265d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265d7-124">CommonParameters</span></span>
<span data-ttu-id="265d7-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="265d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265d7-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="265d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="265d7-127">INPUTS</span></span>

### <span data-ttu-id="265d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="265d7-128">System.String</span></span>

### <span data-ttu-id="265d7-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="265d7-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="265d7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="265d7-130">OUTPUTS</span></span>

### <span data-ttu-id="265d7-131">Microsoft.Azure.Commands.Compute.Models.VirtualMa modelseAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="265d7-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="265d7-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="265d7-132">NOTES</span></span>

## <span data-ttu-id="265d7-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="265d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="265d7-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="265d7-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="265d7-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="265d7-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="265d7-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="265d7-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


