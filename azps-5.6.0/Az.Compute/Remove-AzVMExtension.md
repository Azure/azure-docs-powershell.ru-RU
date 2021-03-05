---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: cc813b4d6b3c5efbd1c54c25b5e198c5b0ce94e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985270"
---
# <span data-ttu-id="6d7f2-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d7f2-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="6d7f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d7f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7f2-103">Удаляет расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="6d7f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d7f2-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d7f2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d7f2-105">DESCRIPTION</span></span>
<span data-ttu-id="6d7f2-106">При этом из расширений виртуальной машины удаляется расширение **AzVMExtension.**</span><span class="sxs-lookup"><span data-stu-id="6d7f2-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="6d7f2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d7f2-107">EXAMPLES</span></span>

### <span data-ttu-id="6d7f2-108">Пример 1. Удаление расширения с виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6d7f2-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="6d7f2-109">Эта команда удаляет расширение ContosoTest из виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="6d7f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d7f2-110">PARAMETERS</span></span>

### <span data-ttu-id="6d7f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7f2-111">-DefaultProfile</span></span>
<span data-ttu-id="6d7f2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d7f2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6d7f2-113">-Force</span></span>
<span data-ttu-id="6d7f2-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7f2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6d7f2-115">-Name</span></span>
<span data-ttu-id="6d7f2-116">Указывает имя расширения, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d7f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d7f2-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6d7f2-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="6d7f2-119">-VMName</span></span>
<span data-ttu-id="6d7f2-120">Указывает имя виртуальной машины, с которой этот cmdlet удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="6d7f2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d7f2-121">-Confirm</span></span>
<span data-ttu-id="6d7f2-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7f2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7f2-123">-WhatIf</span></span>
<span data-ttu-id="6d7f2-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7f2-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7f2-126">CommonParameters</span></span>
<span data-ttu-id="6d7f2-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7f2-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d7f2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7f2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d7f2-129">INPUTS</span></span>

### <span data-ttu-id="6d7f2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6d7f2-130">System.String</span></span>

## <span data-ttu-id="6d7f2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d7f2-131">OUTPUTS</span></span>

### <span data-ttu-id="6d7f2-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6d7f2-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6d7f2-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d7f2-133">NOTES</span></span>

## <span data-ttu-id="6d7f2-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d7f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="6d7f2-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d7f2-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="6d7f2-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d7f2-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


