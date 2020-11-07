---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914201"
---
# <span data-ttu-id="f1600-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="f1600-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="f1600-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1600-102">SYNOPSIS</span></span>
<span data-ttu-id="f1600-103">Удаление (а) (-а) секретных информации из объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f1600-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1600-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1600-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1600-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1600-105">DESCRIPTION</span></span>
<span data-ttu-id="f1600-106">Командлет Remove-AzureRmVMSecret удаляет из объекта виртуальной машины (a) секрет (-ов).</span><span class="sxs-lookup"><span data-stu-id="f1600-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="f1600-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1600-107">EXAMPLES</span></span>

### <span data-ttu-id="f1600-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1600-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="f1600-109">Удаление всех секретов из виртуальной машины "VM1" в группе ресурсов "Rg1" и обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f1600-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="f1600-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1600-110">PARAMETERS</span></span>

### <span data-ttu-id="f1600-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1600-111">-DefaultProfile</span></span>
<span data-ttu-id="f1600-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1600-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1600-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f1600-113">-SourceVaultId</span></span>
<span data-ttu-id="f1600-114">Указывает массив идентификаторов исходного хранилища, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f1600-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1600-115">-VM</span><span class="sxs-lookup"><span data-stu-id="f1600-115">-VM</span></span>
<span data-ttu-id="f1600-116">Указывает виртуальную машину, с которой этот командлет удаляет (а) секрет (-ов).</span><span class="sxs-lookup"><span data-stu-id="f1600-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="f1600-117">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f1600-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1600-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1600-118">-Confirm</span></span>
<span data-ttu-id="f1600-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1600-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1600-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1600-120">-WhatIf</span></span>
<span data-ttu-id="f1600-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1600-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1600-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1600-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1600-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1600-123">CommonParameters</span></span>
<span data-ttu-id="f1600-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1600-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1600-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1600-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1600-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1600-126">INPUTS</span></span>

### <span data-ttu-id="f1600-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1600-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f1600-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1600-128">OUTPUTS</span></span>

### <span data-ttu-id="f1600-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1600-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f1600-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1600-130">NOTES</span></span>

## <span data-ttu-id="f1600-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1600-131">RELATED LINKS</span></span>

