---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4e722e897b23ce1e7ea7c30a6caa393be75f893c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981032"
---
# <span data-ttu-id="61032-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="61032-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="61032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61032-102">SYNOPSIS</span></span>
<span data-ttu-id="61032-103">Сведения о настраиваемом расширении сценария.</span><span class="sxs-lookup"><span data-stu-id="61032-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="61032-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61032-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61032-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61032-105">DESCRIPTION</span></span>
<span data-ttu-id="61032-106">Cmdlet **Get-AzVMCustomScriptExtension** получает сведения о настраиваемом расширении виртуальной машины сценария на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="61032-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="61032-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61032-107">EXAMPLES</span></span>

### <span data-ttu-id="61032-108">Пример 1. Получить пользовательское расширение сценария</span><span class="sxs-lookup"><span data-stu-id="61032-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="61032-109">Эта команда получает пользовательское расширение сценария ContosoCustomScript для виртуальной машины с именем VirtualMa ветвь07.</span><span class="sxs-lookup"><span data-stu-id="61032-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="61032-110">Пример 2. Просмотр представления экземпляра пользовательского расширения сценария</span><span class="sxs-lookup"><span data-stu-id="61032-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="61032-111">Эта команда получает представление экземпляра настраиваемого расширения сценария ContosoCustomScript для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="61032-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="61032-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61032-112">PARAMETERS</span></span>

### <span data-ttu-id="61032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61032-113">-DefaultProfile</span></span>
<span data-ttu-id="61032-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61032-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61032-115">-Name</span><span class="sxs-lookup"><span data-stu-id="61032-115">-Name</span></span>
<span data-ttu-id="61032-116">Указывает имя настраиваемого расширения сценария, сведения о котором получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61032-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="61032-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61032-117">-ResourceGroupName</span></span>
<span data-ttu-id="61032-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="61032-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61032-119">-Status</span><span class="sxs-lookup"><span data-stu-id="61032-119">-Status</span></span>
<span data-ttu-id="61032-120">Указывает на то, что этот cmdlet получает представление экземпляра настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="61032-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="61032-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="61032-121">-VMName</span></span>
<span data-ttu-id="61032-122">Указывает имя виртуальной машины, для которой этот cmdlet получает расширение настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="61032-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="61032-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61032-123">CommonParameters</span></span>
<span data-ttu-id="61032-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61032-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61032-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61032-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61032-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61032-126">INPUTS</span></span>

### <span data-ttu-id="61032-127">System.String</span><span class="sxs-lookup"><span data-stu-id="61032-127">System.String</span></span>

### <span data-ttu-id="61032-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61032-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61032-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61032-129">OUTPUTS</span></span>

### <span data-ttu-id="61032-130">Microsoft.Azure.Commands.Compute.Models.VirtualMa modelseCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="61032-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="61032-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61032-131">NOTES</span></span>

## <span data-ttu-id="61032-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61032-132">RELATED LINKS</span></span>

[<span data-ttu-id="61032-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="61032-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="61032-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="61032-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="61032-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="61032-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


