---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985242"
---
# <span data-ttu-id="1fc39-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="1fc39-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="1fc39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fc39-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc39-103">Удаляет (а) секретные объекты из объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fc39-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="1fc39-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fc39-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc39-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc39-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc39-106">Новый Remove-AzVMSecret удаляет (а) секретные объекты из объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fc39-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="1fc39-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fc39-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc39-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fc39-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="1fc39-109">Удаляет все секреты виртуальной машины "vm1" в группе ресурсов "rg1" и обновляет VM</span><span class="sxs-lookup"><span data-stu-id="1fc39-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="1fc39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fc39-110">PARAMETERS</span></span>

### <span data-ttu-id="1fc39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc39-111">-DefaultProfile</span></span>
<span data-ttu-id="1fc39-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc39-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1fc39-113">-SourceVaultId</span></span>
<span data-ttu-id="1fc39-114">Определяет массив исходных кодов хранилища, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc39-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc39-115">-VM</span><span class="sxs-lookup"><span data-stu-id="1fc39-115">-VM</span></span>
<span data-ttu-id="1fc39-116">Указывает виртуальную машину, с которой этот cmdlet удаляет (а) секретные коды.</span><span class="sxs-lookup"><span data-stu-id="1fc39-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="1fc39-117">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="1fc39-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1fc39-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fc39-118">-Confirm</span></span>
<span data-ttu-id="1fc39-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1fc39-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc39-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc39-120">-WhatIf</span></span>
<span data-ttu-id="1fc39-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc39-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc39-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1fc39-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc39-123">CommonParameters</span></span>
<span data-ttu-id="1fc39-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc39-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fc39-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc39-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fc39-126">INPUTS</span></span>

### <span data-ttu-id="1fc39-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="1fc39-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fc39-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fc39-128">OUTPUTS</span></span>

### <span data-ttu-id="1fc39-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="1fc39-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fc39-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fc39-130">NOTES</span></span>

## <span data-ttu-id="1fc39-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fc39-131">RELATED LINKS</span></span>
