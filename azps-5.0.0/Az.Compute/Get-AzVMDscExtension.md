---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246416"
---
# <span data-ttu-id="c212e-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c212e-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="c212e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c212e-102">SYNOPSIS</span></span>
<span data-ttu-id="c212e-103">Получает параметры расширения DSC для определенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c212e-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c212e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c212e-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c212e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c212e-105">DESCRIPTION</span></span>
<span data-ttu-id="c212e-106">Командлет **Get-AzVMDscExtension** получает параметры расширения конфигурации нужного состояния (DSC) на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c212e-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c212e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c212e-107">EXAMPLES</span></span>

### <span data-ttu-id="c212e-108">Пример 1: получение параметров расширения DSC</span><span class="sxs-lookup"><span data-stu-id="c212e-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="c212e-109">Эта команда получает параметры расширения с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="c212e-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="c212e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c212e-110">PARAMETERS</span></span>

### <span data-ttu-id="c212e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c212e-111">-DefaultProfile</span></span>
<span data-ttu-id="c212e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c212e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c212e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c212e-113">-Name</span></span>
<span data-ttu-id="c212e-114">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c212e-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c212e-115">Командлет Set-AzVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="c212e-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="c212e-116">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzVMDscExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c212e-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c212e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c212e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c212e-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c212e-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c212e-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c212e-119">-Status</span></span>
<span data-ttu-id="c212e-120">Указывает на то, что этот командлет получает представление экземпляра расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="c212e-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c212e-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c212e-121">-VMName</span></span>
<span data-ttu-id="c212e-122">Указывает имя виртуальной машины, для которой этот командлет получает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="c212e-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c212e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c212e-123">CommonParameters</span></span>
<span data-ttu-id="c212e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c212e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c212e-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c212e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c212e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c212e-126">INPUTS</span></span>

### <span data-ttu-id="c212e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c212e-127">System.String</span></span>

### <span data-ttu-id="c212e-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c212e-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c212e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c212e-129">OUTPUTS</span></span>

### <span data-ttu-id="c212e-130">Microsoft. Azure. Commands. COMPUTE. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c212e-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="c212e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c212e-131">NOTES</span></span>

## <span data-ttu-id="c212e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c212e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c212e-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c212e-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="c212e-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c212e-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


