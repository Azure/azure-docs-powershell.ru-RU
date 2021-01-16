---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329002"
---
# <span data-ttu-id="54cf9-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="54cf9-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="54cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="54cf9-103">Получает параметры расширения DSC на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="54cf9-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="54cf9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54cf9-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54cf9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="54cf9-106">Для **параметра Get-AzVMDscExtension** задаются параметры расширения DSC на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="54cf9-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="54cf9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="54cf9-108">Пример 1. Настройка расширения DSC</span><span class="sxs-lookup"><span data-stu-id="54cf9-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="54cf9-109">Эта команда получает параметры расширения DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="54cf9-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="54cf9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54cf9-110">PARAMETERS</span></span>

### <span data-ttu-id="54cf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cf9-111">-DefaultProfile</span></span>
<span data-ttu-id="54cf9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54cf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54cf9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="54cf9-113">-Name</span></span>
<span data-ttu-id="54cf9-114">Имя ресурса Диспетчера ресурсов Azure, представляюца расширение.</span><span class="sxs-lookup"><span data-stu-id="54cf9-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="54cf9-115">Этот Set-AzVMDscExtension задает это имя Microsoft.Powershell.DSC, то есть то же значение, которое используется **в get-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="54cf9-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="54cf9-116">Укажите этот параметр только в том случае, если вы изменили имя по умолчанию в проектлете **Set-AzVMDscExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54cf9-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="54cf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="54cf9-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54cf9-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="54cf9-119">-Status</span><span class="sxs-lookup"><span data-stu-id="54cf9-119">-Status</span></span>
<span data-ttu-id="54cf9-120">Указывает на то, что этот cmdlet получает представление экземпляра расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="54cf9-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="54cf9-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="54cf9-121">-VMName</span></span>
<span data-ttu-id="54cf9-122">Указывает имя виртуальной машины, для которой этот cmdlet получает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="54cf9-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="54cf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cf9-123">CommonParameters</span></span>
<span data-ttu-id="54cf9-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cf9-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54cf9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cf9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54cf9-126">INPUTS</span></span>

### <span data-ttu-id="54cf9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="54cf9-127">System.String</span></span>

### <span data-ttu-id="54cf9-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54cf9-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54cf9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54cf9-129">OUTPUTS</span></span>

### <span data-ttu-id="54cf9-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="54cf9-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="54cf9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54cf9-131">NOTES</span></span>

## <span data-ttu-id="54cf9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54cf9-132">RELATED LINKS</span></span>

[<span data-ttu-id="54cf9-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="54cf9-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="54cf9-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="54cf9-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


