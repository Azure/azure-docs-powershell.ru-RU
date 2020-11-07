---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 9f9b8f28fd3b2597dede1b9fe50780b2c5e43abb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731275"
---
# <span data-ttu-id="f825b-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="f825b-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="f825b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f825b-102">SYNOPSIS</span></span>
<span data-ttu-id="f825b-103">Удаление (а) (-а) секретных информации из объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f825b-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="f825b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f825b-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f825b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f825b-105">DESCRIPTION</span></span>
<span data-ttu-id="f825b-106">Командлет Remove-AzVMSecret удаляет из объекта виртуальной машины (a) секрет (-ов).</span><span class="sxs-lookup"><span data-stu-id="f825b-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="f825b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f825b-107">EXAMPLES</span></span>

### <span data-ttu-id="f825b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f825b-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="f825b-109">Удаление всех секретов из виртуальной машины "VM1" в группе ресурсов "Rg1" и обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f825b-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="f825b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f825b-110">PARAMETERS</span></span>

### <span data-ttu-id="f825b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f825b-111">-DefaultProfile</span></span>
<span data-ttu-id="f825b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f825b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f825b-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f825b-113">-SourceVaultId</span></span>
<span data-ttu-id="f825b-114">Указывает массив идентификаторов исходного хранилища, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f825b-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f825b-115">-VM</span><span class="sxs-lookup"><span data-stu-id="f825b-115">-VM</span></span>
<span data-ttu-id="f825b-116">Указывает виртуальную машину, с которой этот командлет удаляет (а) секрет (-ов).</span><span class="sxs-lookup"><span data-stu-id="f825b-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="f825b-117">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f825b-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="f825b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f825b-118">-Confirm</span></span>
<span data-ttu-id="f825b-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f825b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f825b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f825b-120">-WhatIf</span></span>
<span data-ttu-id="f825b-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f825b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f825b-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f825b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f825b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f825b-123">CommonParameters</span></span>
<span data-ttu-id="f825b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f825b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f825b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f825b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f825b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f825b-126">INPUTS</span></span>

### <span data-ttu-id="f825b-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f825b-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f825b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f825b-128">OUTPUTS</span></span>

### <span data-ttu-id="f825b-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f825b-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f825b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f825b-130">NOTES</span></span>

## <span data-ttu-id="f825b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f825b-131">RELATED LINKS</span></span>
