---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408071"
---
# <span data-ttu-id="dbf80-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="dbf80-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="dbf80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf80-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf80-103">Удаляет расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dbf80-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="dbf80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbf80-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbf80-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf80-106">При **этом расширение удаляется** из расширений виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dbf80-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="dbf80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbf80-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf80-108">Пример 1. Удаление расширения с виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="dbf80-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="dbf80-109">Эта команда удаляет расширение ContosoTest из виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dbf80-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="dbf80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbf80-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf80-111">-DefaultProfile</span></span>
<span data-ttu-id="dbf80-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf80-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbf80-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dbf80-113">-Force</span></span>
<span data-ttu-id="dbf80-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dbf80-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbf80-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dbf80-115">-Name</span></span>
<span data-ttu-id="dbf80-116">Указывает имя расширения, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbf80-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbf80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf80-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbf80-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dbf80-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dbf80-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="dbf80-119">-VMName</span></span>
<span data-ttu-id="dbf80-120">Указывает имя виртуальной машины, с которой этот cmdlet удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="dbf80-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="dbf80-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbf80-121">-Confirm</span></span>
<span data-ttu-id="dbf80-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dbf80-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf80-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf80-123">-WhatIf</span></span>
<span data-ttu-id="dbf80-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbf80-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf80-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbf80-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf80-126">CommonParameters</span></span>
<span data-ttu-id="dbf80-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf80-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbf80-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf80-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbf80-129">INPUTS</span></span>

### <span data-ttu-id="dbf80-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dbf80-130">System.String</span></span>

## <span data-ttu-id="dbf80-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbf80-131">OUTPUTS</span></span>

### <span data-ttu-id="dbf80-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dbf80-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dbf80-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbf80-133">NOTES</span></span>

## <span data-ttu-id="dbf80-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbf80-134">RELATED LINKS</span></span>

[<span data-ttu-id="dbf80-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="dbf80-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="dbf80-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="dbf80-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


